# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-11-09, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Individual Issue Items

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
    * Karl Fogel, Viscount, Orion Arm, @kfogel, <kfogel@AnyPlausibleDomain.com>
    * Mithuna <mkrishna@permanent.org>
    * Andrew <aatwood@permanent.org>
    * xmunoz
    * Dan Schultz <dan@opentechstrategies.com>
    * Jason

## Notes
    * Good News
        * I MADE KIMCHI
        * I found hills in Illinois!
            * (If you're not from here, you might not understand how unexpected that is.)
            * https://www2.illinois.gov/dnr/education/Documents/OnlineIntroIllinoisNatRes(5-6).pdf
        * I MADE AN APPLETINI!
            * I know this is not unique to me but worth writing down: neighbors were literally dancing in the back yard and singing.
        * Talked to an old friend.
        * Got a free pretzel at the brewery I was at over the weekend...
        * Turns out there's such a thing as joyscrolling <3🎉

    * Individual issues
        * Deploy process: ssh access?
            * How do we want to manage SSH access and deployment?
                * Currently: push things to S3; cron job checks for updates, and pulls the tar down if it sees changes. This is a bad way to deploy!
                * We now have an ansible script that is part of our provisioning process.
                * Do we want to open up port 22 to the world?
                    * Yes, with ssh-key-only authentication; Continuous Deployment (CD) is way way better than manual deployment
                    * This is more work; need to:
                        * Review & configure sshd config
                        * Generate ssh key pair for deploy user
                        * Update AWS network config / firewall allowlist
                        * Add CI for GitHub Action
        * Functional test automation
            * make sure the app actually supports all the filetypes we claim to support
            * working on push button, get test
            * working on creating a ground truth that can be checked against to ensure that the conversions are actually happening (not simply that they're not erroring)
            * Cristina needs support in validating what should be happening; could be Robert or Mithuna or Andrew
                * Mithuna is fully booked for this week but will take this on next week.
                * For now, Cristina will just run the test with no validation of the results.
        * Small Sentry questions
            * Dan & Andrew will pair briefly on configuring Sentry with TypeScript in upload-service
        * Lets do a status check on Uploads.
            * Jason: knows what needs to be done and just needs to do it.
                * Days not weeks.  Hopes to have PR ready by tomorrow or Wednesday.
            * Mithuna
                * Finished up the unit tests for the first endpoint; it's in PR mode.
                * Working on the second endpoint now.
        * Cecilia/Dan transition
            * WHAT?!?! jk -- We'll have a 1-2 week overlap (my last day is currently early December)
            * build back better™️
        * Andrew will be out Tuesday and Wednesday this week.
