# Infrastructure Training
28 December 2020

Led by Cristina Munoz

## POP

### Purpose

For Permanent staff to have full understanding of the current infrastructure setup.

### Outcomes

Permanent staff will know how to:

- Deploy new code changes on all three environments
- Update environments (e.g. php version)
- Store/alter secrets
- Debug issues that appear outside of code

### Process

Cristina will go over several areas as listed in https://github.com/PermanentOrg/infrastructure/issues/29

## Attendees

- xmunoz
- Cecilia
- Jason
- Andrew

## Notes

### Local environment and CI!

This partially lives in the github
[infrastructure](https://github.com/PermanentOrg/infrastructure) repo and
partly in the [devenv](https://github.com/PermanentOrg/devenv) repo.

* Why? To preserve the config script across environments.  BUT some steps are
  necessarily different between local and AWS.  e.g. AWS needs ssh keys for
  everyone and locally we do not need those!
* Common config stuff is in infrastructure/provisioners (see Vagrantfile for
  more)
* One aside - we can't use MariaDB because it lacks something (the JSON field
  type?) that is in MySQL (so we add a special apt source for MySQL)
* TODO: look into preload.conf in the templates dir (do we need it anymore?)
* Backend server is doing the most, we run that one locally (skip
  taskrunner/cron)
* This also uses the bitbucket
  [docker](https://bitbucket.org/permanent-org/docker/src/master/) repo
  - note that this includes `perm.sql`, which is a dump of the schema that is
    probably *not* in sync with any of the live schemas, oops, so updating this
    will be part of standardizing those.
  - also has a container for mdot (though we haven't discussed where that is used yet)
* Dockerhub:
  - These images are used by bitbucket pipelines for CI (we could get rid of
    them if we moved entirely to GitHub actions)
  - Locally: we use the `perm.sql` file that lives in the BitBucket docker repo
    to set up the local schema.  Obviously we could move that `perm.sql` file
    somewhere else if we like, in future.
  - The latest containers are the ones in the permanentorg organization and
    they are public https://hub.docker.com/u/permanentorg
  - TODO: remove the now-public images from permanentlegacy and the mdot image,
    since it isn't used by GitHub actions
  - The mysql image is private because it has the creds to the db in it, which
    are the same across environments, boo
* Database repo - an aside, sort of, but this isn't being deployed anywhere

### Making configuration changes

* Actions on GitHub infra repo:
  - All images are made in one action
  - These images appear in AWS as EC2 instances called "packer builder"
    - these will stay running if the image building fails!  Need to be
      terminated manually.  Under normal circumstnaces these are terminated
      automatically once the AMIs are ready.
  - We occasionally get messages from GitHub about being rate limited on the
    AWS api.
  - Can usually just rerun it and it will work. :)  But remember to clean up!
* Terraform
  - Two steps to deploy the AMIs that the GitHub actions built.
    1. Terraform plan
       - This looks for the latest AWS images and compares them to the ones
         currently running.  If their infra is up to date, it tells you and you
         can't do anything else!
       - If there *are* differences, Terraform will display them.  These are the
         best source for debugging if something goes wrong.
         - Can look at the details here, too, e.g. the ids of the old and new
           AMIs and compare them in the aws console
       - Note we keep old AWS AMIs for now (or rather have no automated cleanup
         set up); we should clean this up by deleting the old AMIs
    2. Confirm & Apply
       - NOTE if you deploy an old AMI you must also do a code deploy (because
         code is baked in)

* Wordpress
  - Baked in to the apache config
  - Can probably get rid of .git lines, too, because we believe we aren't even
    packaging that up anymore
  - Some (most?) of the Apache config will end up as path based rules in the
    AWS Elastic Load Balancer

### Code deploy!

* BitBucket multibranch system
* Example of deploying to staging:
  * Merge code into dev as we go
  * Create PR from dev to staging, let pipeline run, merge PR into staging
  * Go to infra GitHub repo, launch a staging code deploy from actions

### Secrets

* Some of these live in BitBucket, others in GitHub
* GitHub has some in the infra repo and some at the organization level, which
  are accessible to all repos in the org
  - `DEPLOYER_PRIVATE_KEY` is the ssh key for the `deployer` linux user in the
    AMIs
* Also in Terraform!
  - This also needs AWS access and build keys.  The AWS build key is in
    BitWarden since it is used in a lot of different places.  We can configure
    it in the IAM dashboard.
  - We should probably plan to rotate these keys periodically

### Local vs AWS

* Can compare these via infrastucture/images
* Note that the build script step takes a long time / is complex on AWS,
  Cristina recommends downloading the output from the GitHub Actions tab if we
  want to parse any output
* NOTE: build script might exit with 0 (and look fine to Ansible) even if it
  errored for some reason. Make sure to check this locally!
* Changes that run across environments should go in setup.yml if possible

### Changing the deployment process

* AWS servers only: Change the deploy scripts (in provisioners)
* Local dev only: Change the devenv `bin/deploy.sh`
* Both AWS (backend server) and local: `configure.sh` gets run for both

### Best practices / troubleshooting

* Log into the server while deploying so you can make sure that each process
  only has one instance running at a time (the daemons, that is)
  - my hunch is just a timing thing with the PID files that control the
    daemons, start + stop separately is enough time between but restart moves
    too quick *nod*

### Networking

* We have a static ip for the "backend" server so the load balancer can find it
* Cron and taskrunner have no web frontend so they don't need to stay in the same place

### "scripts"

* This builds an ansible inventory file
* It specifies the name of the server (gotten from AWS) so that it can then ssh
  to it and deploy the code.
* This script could be better / less brittle.  See issue #21 in the infra repo.
