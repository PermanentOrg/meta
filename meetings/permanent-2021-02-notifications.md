Previous work:
	* Team kick-off: https://pad.riseup.net/p/permanent-2021-01-notifications-service
	* Research alternatives: https://permanent.atlassian.net/browse/PER-8250
	* Design database schema
		* https://pad.riseup.net/p/permanent-2021-02-notifications-schema
		* https://docs.google.com/spreadsheets/d/1Axp6jk_E5sEDzVOBNlwIww0MQEZI5FxvGSryBmnhhlU/edit#gid=697288786

Partially complete work:
	* Design doc: https://github.com/PermanentOrg/notification-service/pull/4
	* Database migrations: https://github.com/PermanentOrg/notification-service/pull/7

Discussion
	* How do we want vagrant to work? Windows can't map node_modules correctly; neither Jason nor Mithuna want to develop inside of vagrant. We can make it expect the notification service to be running on the host, and refer to the host by IP address; but that makes it a little bit harder to go from 0 to working Permanent application
		* Let's run the notification service on the host.  Down the road, let's make it optionally run in vagrant as well (imagining the case where someone isn't actively working on the notification service and just wants it to work inside their local box)

Unassigned work
	* Deploy notification-service
		* https://github.com/PermanentOrg/infrastructure/issues/45
			* We want to do this sooner rather than later, even though the service doesn't do anything yet
		* Mithuna will take a first pass at this
	* Vagrant (per above conversation)
		* Jason to create an issue
	* Create RDS DBs
		* https://github.com/PermanentOrg/notification-service/issues/10
			* This will yield some credentials which should be stored as secrets available to the service
			* M and J to pair
	* Add API endpoints for notifications
		* https://github.com/PermanentOrg/notification-service/issues/11
		* M and J to pair on first one, then Mithuna to pick up the next one
	* Call new notification API from PHP code
		* Mithuna has figured out where it should go, we just need to write it!  (At the end of Post to create an account)
		* Mithuna can do this!
	* Front-end gets a list of notifications from the new service (via PHP proxy) and integrates it into the list
		* Deferring until later this year; not part of Q1 goal
		* Instead, we'll focus on push notifications
	* Push notifications

Week 0 (week of Feb 22)
- PR for deploying the service
- Creating the databases
- Making sure M and J can each run this locally and have it talk to the rest of the app appropriately
- Call the health check from the php code (with a feature flag so it isn't dependent on deploying the service first)
- First endpoint! (Create, possibly spilling into next week)

Week 1
- Remaining "hello world" endpoints
  - Mark as read (update)
  - Get a list (read)
- Research including Firebase for push notifications
  - How to register a device?
  - How to send a notification?
  - Does Firebase return a "notification read" response?
  - Do we need to keep track of a "device ID" or like an "apple account ID" / "android account ID"? Can a user have multiple device IDs? Can a user have multiple account IDs?
  - Will need to come up with enough of a spec to hand off to the mobile team
  - How do we test this? Does Firebase offer good testing tools without needing to run an app on a mobile device?

Week 2

Week 3

Week 4

---

This is an etherpad service hosted by Riseup. Riseup provides secure online communication tools for people and groups working for liberatory social change.

Riseup depends on donations from users like you to keep going. Please visit https://riseup.net/donate to contribute.

WARNING: This "pad" is a collaborative document that can be edited by anyone who has the URL. If you use an obvious name for the pad, it could be guessed.

WARNING: This pad will be DELETED if 60 days go by with no edits. There is NO WAY to recover the pad after this happens, so be careful!

If you want a pad to be kept for up to one year (365 days) without edits, append the word "-keep" to the end of the pad name.

If you want a pad to be deleted after one day, append the word "-tmp" to the end of the pad name.

For example:
* https://pad.riseup.net/p/1234-tmp => deleted after 1 day of inactivity
* https://pad.riseup.net/p/1234 => deleted after 60 days of inactivity
* https://pad.riseup.net/p/1234-keep => deleted after 365 days of inactivity

Abusive behavior is not allowed on this service. Please visit https://support.riseup.net to report any problems.
