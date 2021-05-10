# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-04-19, 11am CT
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
	* Mithuna mkrishna@permanent.org 
	* Cecilia
	* Jason but his laptop is sad

## Notes
                        
* Good News
	*  Only bad news: Hail damaged our car.
	*  Family coming this week!
	* Vaccine appointment :)

* Open PRs
        * GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
        * BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org

* Priorities for the week
	* https://permanent.atlassian.net/browse/PER-8307
	* Increased occurrence of "stuck in processing" lately?
	* Cecilia
		* registerRecord cleanup for GFTW
		* share bug
		* review system exception PR
	* Mithuna
		* NS #15 Register device tokens - will try for 10more mintues else pair with Jason
		* https://bitbucket.org/permanent-org/back-end/pull-requests/19/register-a-device-token 
			* Try and see if sentry error are showing here or we can throw.
			* Refactor with helper class method in register device and notification creation code
		* Have backend call notification service while sending Shared folder notification email.Initially missing full context, just send "you have access to a new folder" and take them to the list of shares. Create a jira. 
		* Create a confluence page about first response steps on a hourly upload error.
	* Jason
		* notification-service firebase credentials PR to infrastructure
		* notification-service send push notification PR
		* 
		* gftw

Goal: send a push notification!
	* Mithuna will move back-end PRs through review
	* Jason will create PRs for infastructure and to actually send a push notification
		* not a priority for *this* week: send context with a notification
	* Account creation is our "hello world", but can't actually result in a push notification since the device token is not registered by that point; what do we actually want to send?
		* https://docs.google.com/spreadsheets/d/1QLCspBzZfq21TG32KXoSRFTVz7UZ-3n8TnYVzOeElIc/edit
	* Question for mobile team: is it better for them to send data as flat key-value pairs or one key with a value that is json encoded as a string?
		* Jason will write in #public-mobile-dev
	* For the purpose of making sure data flow works and we have something to demo, we will start with the "you have access to a new folder" notification, without additional context

List of notifications is in the "Mobile Pre Release" tab here: https://docs.google.com/spreadsheets/d/1QLCspBzZfq21TG32KXoSRFTVz7UZ-3n8TnYVzOeElIc/edit#gid=469627093
