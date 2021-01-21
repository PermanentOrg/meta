Roll Call
	* Robert
	* Cecilia
	* Jason
	* Bryson, Andrew, Mithuna

Framing
Purpose
	* Build (Design) a debuggable, testable, documented, maintainable, open source notifications system to replace a set of notifications that grew organically over the life of the app.
	* This meeting: decide what we want this new system to look like
	* Robert: What should notifications look like?
	* Andrew: leaving no stone unturned of a top level view of what notifications project will be;
	* Cecilia: catching potential problems / trip-ups before we start the notifications project in earnest;
	* Jason/Mithuna: making sure that we're all aligned on requirements; particularly, unified vs per-archive notifications
	* To get on the same page about what the notification project will be
Outcomes
	* Full team understands/agrees with the scope of this project
Process
	* 

Agenda

What is it?
	* consolidate activity and notification?
	* adding share notification into the activity feed?
	* Build Bryson's activity feed design?
	* Is it a modular vertical service?

From Jason
There is a difference between an acitivty feed and notifications and we need to decide which we are building.
	* notification: actionable notice, informational (system needs user to know);
		* 
	* activity feed: never ending scroll of things people on the system are doing – surfacing the behavior of other users;
		* actions: commenting, liking, viewing;
	* Also, audit log is part of this

Summary
	* we want to build Bryson's Activity Feed design
	* we're going to create a new service to do it
		* existing notification system will persist and will be slowly replaced by a new service;
	* We should start with what is most important to the User
		* welcome message (hello, world!)
		* member invitations
		* share invitations
		* recieve approve share request
		* low storage warning
	* Things to consider
		* we don't always want to send an email for all notifications
		* we may want other notification channels in the future (SMS, push, etc.)
		* users may not always want to receive emails we send
		* non-users and users both get notifications (messages will differ)
		* notifications from before you created an account may need to be surfaced
		* users (and non-users) might want to subscribe to archive feeds (RSS?)
		* security notifications may require a separate authentication service

What's most important to the user?
	* low storage!!!
	* notifications where users are interacting with each other
		* share a file/folder
		* invite to be a member
		* recieve/approve share request




	* Moving of files and folders
	* Share requests

	* Discuss about  notifications from a user perspective. Talk through it and make sure it make sense.
		* What was Bryson's original vision for this activity feed?  Where did it come from?
			* Intended to be a one-stop-shop for user activity (Cecilia's words)
			* But the original design grew out of a surface-level understanding of notifications (per Bryson)
		* There are many different kinds of notifications

	* Do we need to unify the notifications or leave it per archive?
		* Robert: we want to unify; we don't want users having to flip from archive to archive to "find their notifications"
		* "Notifications are to human beings" but "Activities are between Archives"

	* Share notifications - Filter the types for necessary for  UI.

	* Emails are currenty the main contact method to user. but not all emails are registered in notifications. Needs discussion.

## Kinds of messages we send:
    * messages to users
    * invitations to non-users (and anything else?)
    * messages to new users who accepted an invitation (so have a record before they create an account) (e.g. they got an invitation, made an account, then already had a message in their activity feed about becoming a member of an archive owned by the person who invited them)
    * RSS (or similar) to non-users who don't intend to become users but want to follow a public archive (FUTURE)
    * 

Design Docs
	* https://docs.google.com/document/d/1GZpF06d99IL_p2wcwlyPKfkpv4OQqYUhHAiaCLqVAZc/edit#heading=h.v8ajvfny3enf
	* https://docs.google.com/document/d/1x8Ewbks7Lsigk6ZQGVmbZH_UqJOQboL5bCiDL84-QGg/edit#
	* https://docs.google.com/document/d/1-lIM5J79PaRM60pOwOjYN5iIK0jL_mFmwova2vAqeHQ/edit#

In-App Parity
	* https://docs.google.com/spreadsheets/d/1r3QIK2xsea3AMCRU2WVShydRSdITQhc4tkbiW4DtmCw/edit#gid=0
