# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-01-11, 11am CT
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
- Cecilia
- Jason
- Andrew
- Mithuna


## Notes
    * Good News
    Mithuna: Snowwwwwww.. lots and lots of snow
    * Individual issues
	     - Upload status?
			- Sprint moving around / not accounting for everything at the beginning.  Thoughts?
				- examples: making videos for virtual conferences, ongoing assignments to Andrew from mobile team meetings
		Mithuna
		- What is pending in uploads
			- PRs are still open
				https://bitbucket.org/permanent-org/library/pull-requests/110
				https://bitbucket.org/permanent-org/api/pull-requests/287
				https://github.com/PermanentOrg/web-app/pull/2
				https://github.com/PermanentOrg/devenv/pull/18
				https://github.com/PermanentOrg/infrastructure/pull/36
				https://github.com/PermanentOrg/upload-service/pull/26
			- Functional test needs to be updated to use new upload flow
				https://github.com/PermanentOrg/functional-test/issues/5
		- What are the testing procedures/ should we create a test document?
			- Yes!  Mithuna will create an initial version and everyone else will add on
			- Think about: edge cases, integrations
				- known issue: drag n drop multiple folders at once
				- FamilySearch: can use their sandbox/beta envs, Andrew will check to see which environments of ours point to which environments of theirs so we can test effectively
				- node-sdk test scenario
		- When can we release
			- Let's aim to get it on dev this week
			- Note that unit tests are still failing on one of the PRs
				- An expected failure is about importing the uuid library (introduced in library pr and used in api pr)
		- Should we do thorough test in staging?
			- Yes, and remember mobile team is using staging for their work
			- Question for Cecilia and Andrew: what will mobile team need to change for new upload?
				Jason still needs to review https://permanent.atlassian.net/wiki/spaces/EN/pages/793051137/API+Guide
		-Jason : Anything in pipeline we need to worry about for deployment?
			- API error changes for mobile, tag search PR, Cristina's system exception PR(s).  Would prefer to get those out first.  We expect the upload deployment to take at least a week to move through environments.
		- Does anyone outside of our team need to verify anything before we go to prod?
			- TheirStory, but we can test the SDK ourselves
			- Robert will probably want to try it once on staging
	-  Need to change the functional test as it is still pointing to the old upload endpoint https://github.com/PermanentOrg/functional-test/actions
	- Tests fail when run twice because we're not creating an account ID 1 for orphan account curator
	  - originally thinking of adding seed data to perm.sql
    - https://github.com/PermanentOrg/functional-test/blob/e803c5fabbcbd4a5ffea97447e65c3f69bf1d486/run_test.py#L117-L133
    - CI can't make a curl call, would have to call php some other way (no webserver running).  Note could do this at Docker image creation time for CI, instead of at test run time. 
    - software for recording videos: OBS Studio https://obsproject.com/
	
	
Followup convo:
    - Jason plans to clean up web-app PR then would prefer a review from Andrew (will tag Andrew in the PR once it's ready for review)
    - We should all do reviews on all the PRs
