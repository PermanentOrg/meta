# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-04-05, 11am CT
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


## Notes
                        
* Good News
	* New patio furniture coming!
	* First tomato 
	* It's been so sunny and warm! Yay spring
	* 

* Open PRs
	* GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
	* BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org
		* Removing device code - Jason is leaving behind more code in order to maintain the old iOS app
			* See this for intended next step: https://permanent.atlassian.net/wiki/spaces/EN/pages/1447067649/device
		* 

* Interview planning: https://docs.google.com/document/d/1FD6Odrh7OvWNyg6KHVbyB8BTo3oubY2lgXEE5SMn_2Q/edit

* Priorities for the week
	* Cecilia
		* Interview!
		* GFTW
			* Get Jason SDK changes by midday (Central) Tuesday
			* Read/respond to draft report
		* Get Jason prod access
		* Deploy:
			* notification service
			* db changes
		* PR review
			* esp. Fix Formatting https://github.com/PermanentOrg/infrastructure/pull/50
		* Bitrise for mobile
	* Mithuna
		* notification-service#23 resolve conflict
		* Backend#3: 'Welcome to permanent'
			* Notification needs changes in notification service.
		* Rebase and Run eslint on notification-service#25
		* Run eslint on notification-service#25
		* Create device/new which calls the notification service registerToken and saves the token in DB. Duplicates allowed. 
	* Jason
		* Double-check syntax of SimpleVO and edit device confluence page
		* Interviews
		* Finish up https://bitbucket.org/permanent-org/back-end/pull-requests/7/remove-device-code
		* GftW
			* Respond to James's comments on GitHub about deployment
			* Review James's draft report; add requested comments about Etherpad community work
			* Implement all the things: UI, sync, Coil integration
			* Add documentation
		* Review https://github.com/PermanentOrg/node-sdk/pull/17
		* Add database credentials to notification service deployment; pair with Mithuna

Goal: demo creating an account and seeing a notification in the notification service database on dev (Friday afternoon)
