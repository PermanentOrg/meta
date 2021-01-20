2021-01-19

# Notifications

Attendees:
    - Jason
    - Cecilia
    
Purpose: Account for all possible front-end actions when designing the notification back end.

Outcomes: Design, back-end team and front-end team are aligned on next steps for notification design and implementation.

Process:
    - Review back-end notification meeting: https://github.com/PermanentOrg/meta/blob/master/meetings/2021-01-14-notifications.md
    - Come up with a list of all the possible action buttons that would appear on the activity feed
    - Consider all the information the front end would need for each of those action buttons
    
Design Docs
- Unified In-App Notifications https://docs.google.com/document/d/1GZpF06d99IL_p2wcwlyPKfkpv4OQqYUhHAiaCLqVAZc/edit#
- Action Buttons https://docs.google.com/document/d/1x8Ewbks7Lsigk6ZQGVmbZH_UqJOQboL5bCiDL84-QGg/edit#heading=h.2xetx6ndytca
- In-App Share Notifications
https://docs.google.com/document/d/1-lIM5J79PaRM60pOwOjYN5iIK0jL_mFmwova2vAqeHQ/edit#heading=h.2xetx6ndytca

## Notes

	* Notifications are to be account level not archive level
	* call to action buttons: which buttons notifications should have which buttons?
		* what are all the _types_ of actions buttons that could occur?
		* accept / decline; view / ignore; ...?
		* download
	* Bryson: this (types of action buttons, or notifications?) will overlap with mobile
		* B is creating a legend for icons that represent different types of notifications that people might get in mobile
		* Notifications settings page has 5 types of notifications already, plus system notifications, so each of those might get a separate icon ( on mobile)
			* (existing) Categories: account, apps, archive, relationships, share
		* Current plan for mobile MVP is *not* to include action buttons; long term we do want to have that functionality
		* "Download ready" does not fit into any of those categories
	* Mobile vs web:
		* Need to be able to degrade so that we can send notifications that don't have action buttons (in case mobile lags significantly behind desktop and doesn't have buttons for a while)
		* Cecilia doesn't think mobile will lag significantly, though
	* "clean_up_bad_upload"? hopefully will not happen in new upload flow. (side note: this comes from `CleanupBadUploads`; we should see if we can delete that after new uploads are merged)
	* formatting of notification text? currently the text comes straight from the db; if this is important, we can engineer to support that
		* options: save plain text to db; save markdown to db; have each client piece together the message from a template ID and the relevant data
			* As this gets more complicated we may have to duplicate work across client platforms
			* And note that translation/i18n may become an issue down the road, as we're making this decision
	* what if action buttons were just links?
		* that's the plan for mobile MVP
		* we are planning on sending enough information for that to happen
		* probably simpler to build than allowing arbitrary actions in the notifications
	* have we gotten feedback from users about notifications? are they even very well known? how obvious is the dot?
		* Jason thinks we could find out how many notifications are unread by account / percentage of notifications that remain unread / how old are the oldest unread notifications (other possible queries, etc)
	* What's the biggest problem with notifications?
		* They're not visible enough (Bryson)
		* Not all notification types show up in activity feed (Cecilia)
		* Notifications from different archives don't show up in the activity feed (Andrew)
			* WHICH IMPLIES extra complexity for action buttons: if you want to approve something in a different archive (that you're not checked in to) the back end needs to silently switch you to that archive, complete the action, then silently check you back into your previous archive
		* If we show all notifications from all archives together, then we definitely need per-archive notification settings

## Action Button List
	- view
	- add storage
	- accept
	- decline
	- block
		- this does not yet exist, but it needs to: otherwise share invitations are an abuse vector
		- Should this be a button?  "Report"?  Or should it live somewhere else?
		- What about the person who was blocked (blockee)?  What's the UX for them if they try to share with the person who blocked them (blocker)?
	- download
	
	(See https://docs.google.com/document/d/1x8Ewbks7Lsigk6ZQGVmbZH_UqJOQboL5bCiDL84-QGg/edit#heading=h.2xetx6ndytca for specific responses we might send for specific notifications)
	
	button transitions: from "Accept" to "(check) Accepted", from "Decline" to "(x) Declined"
	
	what if there are too many buttons for a single action? might want to spill over to a "..." menu
	
## Questions for full-team brainstorming
	- Do we for sure want to have all notifications for all archives appear together?
