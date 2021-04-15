# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning 2021-04-12, 11am CT 
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose:
Engineering team gets in synch on this week's goals and this sprint's status

## Outcome: 
* Review current status of some active tickets involved in recent work

## Process (Agenda)
* Share any good news ya' got!
* Sprint Review
* Open PRs
* Individual Issue Items


## Roll Call
	* Mithuna
	* Jason
	* Cecilia

## Good news
	* Feels happy my dance shoots went well.
	* Hung out on our patio couch!
	* Made dinner plans with a friend (in three weeks)

## Notes

### Open PRs
GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+

BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org

### Priorities
	* Notification service
		* Milestone: https://github.com/PermanentOrg/notification-service/milestone/1
		* Load service with database https://github.com/PermanentOrg/infrastructure/pull/52 (today!)
		* Register devices 
			* API change https://permanent.atlassian.net/wiki/spaces/EN/pages/1447067649/device (Mithuna will open a PR for this on Wednesday)
			* Notification service change: https://github.com/PermanentOrg/notification-service/pull/25
		* Send notifications to Firebase
			* Includes more secrets (Jason, midweek)
		* List of notifications: https://drive.google.com/file/d/1oGbJhELrgtV25cNGQrBhKi3JdZYWOxfP/view 
			* Note that microservices auth will block any of these that come from cron and taskrunner; we broadly estimate that fixing the auth and deploying notification-service on the real internet would be a 6 week delay
				* All reminders and share summary are run on the cron machine
			* Device-new is not a real email / doesn't exist
			* https://permanent-org.slack.com/archives/C01AK4233TN/p1617939911046200
			* https://docs.google.com/spreadsheets/d/1NNwDlI-ZQTWZFvGbTMWQrCZxW6X_rSlcoeGHPGNZgXs/edit#gid=1764763722
			* https://docs.google.com/spreadsheets/d/1QLCspBzZfq21TG32KXoSRFTVz7UZ-3n8TnYVzOeElIc/edit#gid=1764763722
			* https://docs.google.com/spreadsheets/d/1-SanAhI86qvJulZztSxMHznF6qTLd_l7te4mWFz9Oqs/edit#gid=0
		* Question for mobile team: was this resolved?
			* https://permanent-org.slack.com/archives/C01AK4233TN/p1617294658030900
	* Cecilia
		* Wordpress
		* Prod deploy
		* Test, build image, dev deploy for notification service database
		* GFTW: registerRecord in SDK
		* Access for Jason: AWS (by user group?), Firebase, RDS, Bitwarden?
		* Refresh-after-upload on Chrome
		* PR review
			* check new notification when Mithuna is ready
	* Jason
		* GFTW: https://github.com/PermanentOrg/node-sdk/pull/19
		* GFTW: https://github.com/PermanentOrg/node-sdk/pull/18
		* GFTW: registerRecord once Cecilia finishes
		* Notification service - wire up Firebase
			* Add dependency to notification-service
			* Add env vars to infrastructure
	* Mithuna
		* Creating a notification
			* https://github.com/PermanentOrg/notification-service/pull/27
			* https://bitbucket.org/permanent-org/back-end/pull-requests/3/welcome-to-permanent-notification
		* Register device tokens
			* https://github.com/PermanentOrg/notification-service/pull/25
		* Review https://bitbucket.org/permanent-org/back-end/pull-requests/16/remove-dependency-on-smarty-templating
		* API change for register device tokens  https://permanent.atlassian.net/browse/PER-8299 (see above)
		* Review https://github.com/PermanentOrg/upload-service/pull/34 


Goal for the week: send the welcome notification to Firebase for real!
