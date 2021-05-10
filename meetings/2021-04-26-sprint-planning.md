# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning 2021-04-26, 11am CT 
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei

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
	* Jason
	* Cecilia
	* Natalie
	* Mithuna

## Good news
	* I got my first vaccine! yay!congrats!
	* I had a great vacation
	* Starting my new job!
	* Visited Muleshoe bend to see bluebonnets.

## Notes
	* Welcome Natalie!
		* Small amount of history/context
			* OTS' role
		* Overview of current projects
			* Grant for the Web
			* Notifications
				* Firebase credentials deployed to dev and staging (not prod yet)
				* We can send messages to a device token!
				* Mithuna's device token code is on staging
			* Mobile apps
				* Prepping for initial release
			* Uploads
				* https://www.permanent.org/blog/upgrades-to-uploads/
	* Security issue
	* Backlog pruning - can we close these as done?
		* https://permanent.atlassian.net/browse/PER-7536
			* closed as won't fix
			* we want to move or duplicate https://permanent.atlassian.net/browse/PER-7604 - manual review is still a mystery
		* https://permanent.atlassian.net/browse/PER-8024
			* Moved one item for prospective work out of this epic and into the Uploads Cleanup one
		* https://permanent.atlassian.net/browse/PER-8160
			* We are planning to do this; Mithuna has been working on it :)
	* 

### Open PRs
GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
	* Cecilia will assign a few of her PRs to Natalie to review
		* web-app#22
		* wep-app#21

BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org
	* Cecilia will review back-end#17

### Priorities
	* Jason
		* disable call to vulnerable dependency
		* notification-service: finish send messages PR
		* PR reviews
		* GFTW
	* Mithuna
		* Finish up PER-8324, notification creation on share folder.
		* Add more priority1 notifications. (https://docs.google.com/spreadsheets/d/1QLCspBzZfq21TG32KXoSRFTVz7UZ-3n8TnYVzOeElIc/edit#gid=469627093 second tab)
			* Big change needed here is adding context
			* See Jason's conversation with Vlad - don't want arbitrarily deep JSON here.  Add validation to make sure that we have string key - string value pairs.  Also validate that we're not accidentally using any reserved keys.
		* Design doc for admin panel.
		* https://permanent.atlassian.net/browse/PER-8291
	* Cecilia
		* Natalie!
		* GFTW - esp. pad token
		* PR review
	* Natalie
		* Get everything set up
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
