# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-05-04, 11am CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in sync on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Individual Issue Items
    * Open PRs
--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
	* Cecilia
	* Jason
	* Natalie
	* Mithuna

## Notes
                        
* Good News
	* I had dinner with a friend last night!
	* Went to a restaurant for the first time in forever
	* Bought some baby stuff :)
	* Husband finished another semester.

* Open PRs
	* GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
		* PR 30 - Mithuna will test locally
		* PR 22 (web-app) - Cecilia will make suggested code cleanup
		* PR 21 (node-sdk) - Jason will look back over, needs cleanup in any case
		* 
	* BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org
        
* Projects
	* GFTW
		* Two open PRs on Permanent side need some cleanup
		* Jason has some remaining work on Permanent Etherpad side (https://github.com/PermanentOrg/ep_permanent_exporter)
	* Notifications
		* Mithuna 
			* Want to finish off all the priority one notifications by this week.
			* PR 30 - Mithuna will test locally
			* PT 31 - Jason need to review 


* Priorities for the week
	* Jason
		* PR review
		* wrap up GFTW work needed for demo (pad.staging.permanent.org)
	* Cecilia
		* Prod deploy
		* GFTW cleanup
		* Mobile team apple link file
	* Mithuna
		* PR- 30
		* Zoho
		* Merge PR 31
		* Finish off priority1 notifications.
	* Natalie
		* Public folder thumbnails
		* Cecilia will also send over the "refresh on upload" bug
		* Jason will find and send Natalie docs on turning on debug for web-app

* Need help
	* Mithuna Zoho Integration not working 
		* https://permanent.atlassian.net/browse/PER-8325
		* For reference: https://github.com/PermanentOrg/meta/wiki/Releases#dec-10-2020
		* Probabily cron name has changed or the new infrastructure changes.
	* How to handle one-off data changes?
		* https://permanent.atlassian.net/browse/PER-8329
		* Cecilia will put her in-progress script on GitHub (probably in a new private repo, though Jason also suggested a gist!)
	* CVE : Our deployment should update to new version and if so we should revert the last commit.
	* Web-app linting: Natalie was thinking of adding new rules for new code only (e.g. no more "AnyType")
		* Could use an Angular-specific ruleset
	* Jason - possibly cleanup deployment of back-end repo
