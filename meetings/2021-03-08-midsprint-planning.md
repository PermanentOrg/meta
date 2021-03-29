# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-03-08, 11am CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in sync on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Individual Issue Items
--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---


## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.

	* Jason
	* Mithuna
	* Cecilia


## Notes
	* Good News
		* Jason: I got to play board games with my friends on Saturday!
		* Cecilia: warm(er) weather!
		* Mithuna : Prepped my garden.. It is kind of late but still I might have enough time this season.
        
* Individual Issues
	* Notifications update (refer back to https://github.com/PermanentOrg/meta/blob/main/meetings/permanent-2021-02-notifications.md - how did the Firebase research go?)
		* Jason to do the Firebase research
		* Mithuna to lead on RDS database creation, though J and M will pair
		* Mithuna's infra change to go out
			* Post-review, of course
		* 
	* Deployment: account deletion fix needs to go out, anything else?
		* Mithuna will deploy later today!  Huzzah.

	* https://bitbucket.org/%7Bfda620af-6c76-4a0a-9505-4da3c1f00e34%7D/%7B50d886f9-6de5-489e-bcf8-24bfee03cfa9%7D/addon/pipelines/home#!/results/14 Failing unit test.
		* We believe this is failing because the notifications-service isn't in CI, but we're actually not sure how to change the Docker build for CI!  To be investigated.
	* Notifications service deployment
		* Create RDS databases
		* Deploy Mithuna's infra change
		* THEN check the service is running
		* IDEA: set up a global healthcheck through the PHP API that's available to the world
			* is PHP API up?
			* can we hit the (main) database?
			* is upload-service up?
			* is notifications-service up?
			* eventually, we could have a pretty semi-user-facing status page; Robert has requested a staff-only status page that has more detail about eg the processing queue and such


        
## Followup

