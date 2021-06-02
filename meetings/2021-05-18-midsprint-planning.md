# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-05-18, 11:45am CT
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
	* Natalie
	* Cecilia
	* Jason

## Notes
* Prod deploy today
                        
* Good News
	* Successful second vaccination!
	* Getting really excited about baby!
	* I got an accordion

* Open PRs
	* GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
		* Assign dependabot PRs:
			* Jason: ep_permanent_exporter and notification-service
			* Cecilia: donations-firebase and node-sdk
			* Natalie: upload-service
		* Thumbnails PR is ready for re-review from Cecilia
		* GFTW PR needs cleanup and review from Cecilia and Jason
	* BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org
		* Jason will merge #1
		* Cecilia will review #37
		* Jason needs to add names (archive and account) to #43 and then merge
		* https://bitbucket.org/blog/docker-v20

* Jira
	* Move Natalie's tickets around now that she has a better sense of how hard things are
		* Natalie confirmed that the Google Maps API key is still valid
			* We, however, are not using it.  I (Cecilia) think it's okay to publish it in our history anyway, because it's unlikely to cause any problems (if it does, it's because a bunch of incorrect things happened)
			* Natalie will comment and close as wontfix
		* PER-8198 and PER-8199 are likely to be fixed by the same change(s)
	* Make sure Jason and Cecilia's work is reflected in Jira

* Priorities
	* Cecilia: mobile team unblocking
		* Waiting on Catalin (QA person) to get us a better repro recipe for the session/mfa bug
	* Cecilia: roadmapping / design planning
		* Account/archive decoupling
		* Funding archives
		* Editable tags
		* Auth!
		* Notifications next
		* User onboarding?
	* Jason
		* ep_permanent_exporter and notification-service dependabot PRs
		* merge back-end#1
		* Finish back-end#43 - add names
		* Add documentation to infrastructure from PR to actual README or so
		* GftW
	* Natalie: tickets!
