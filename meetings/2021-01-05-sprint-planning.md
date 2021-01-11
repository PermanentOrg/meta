# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning 2021-01-05, 11am CT Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose:
Engineering team gets in synch on this week's goals and this sprint's status

## Outcome: 
* Review current status of some active tickets involved in recent work

## Process (Agenda)
* Share any good news ya' got!
* Sprint Review
* Individual Issue Items

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
- Cecilia
- Andrew
-Mithuna
- James
- Jason

## Notes

* Good News
	- Going skating tonight!
	- Minimal side effects for my wife's first vaccine dose (maybe scientists know what they're doing after all)
	- Joined a new dance class.

* Sprint Review (add your notes)
- Too many things in sprint right now, need to remove some
- Reassigning some tickets from Cristina
- This sprint was weird.  It was long.  There's too many thing in the sprint rn so we should remove some.
- CK moved some xtina tickets to "unassigned".  Somebody needs to pick them up.
- Mithuna
	- 8041 unit tests: will try to get to
	- 8016 .TIF uploads: Mithuna/Andrew can't reproduce.  CK will take it. .TIF uploads matter.  Andrew notes that thest .tif files are 500mb.  They're pretty big.  Mithuna says they took a while but succeeded.  Perhaps users are timing out from impatience or connection and this is an interface issue, not a backend issue.
	- 8134 MySQL error: Andrew will take; the UI needs to match the database, not the other way around
	- 8142 Email content for share has wrong message: Mithuna may investigate; not sure if we'll get to this. CK wants to timebox this, as it's not terribly urgent
- Jason
	- 8029 upload frontend: needs testing, and needs git history cleanup, but there are no known outstanding issues and the code itself should be ready for testing
	- 8117, 8156: kinda big; might need to split these out into smaller tickets
	
- Cecilia
	- 7971 staff-system-monitor: CK will do more work on this
	- 8123 sentry error: haven't started yet, but doesn't look too complicated
- Andrew
	- 8119 blog homepage spinning: we will defer; still planning to get rid of WordPress. CK estimates SquareSpace will be ready in Feb; complications include donations, mdot sign-in. Then we'll have a project of deleting WordPress from everything - that's the part that's likely to be in mid-Feb
	- 8127, 8134 sentry errors: Andrew has some context, and picked up
	- 8135 filename mismatch: yes good
- unassigned (we miss you, Cristina!)
	- 8090 system exception cleanup: needs review/testing, but seems like the right direction to Jason and Andrew; assigning to CK
	- 7876, 7877, 7878 open sourcing mdot: assigning to Andrew; will probably be some followup conversations
	- 8160 new uploads load test: none of us have worked on this; need to update the code to match the new upload flow. haven't been running regularly because that has budget implications. will defer
	- 8096 rolling db creds: good practice; CK will do
	- 8089 logrotate: Andrew has some context; happens during a failed state - logs fill up with errors. need to identify the underlying issue. will defer
	

* OKRs
	- regroup; lot of change in the last six months. finish up big work: squarespace, uploads
	
	- fix things that people have asked us to fix! (And then tell them we fixed it!)
	How do users give feedback?
		ZohoDesk support
		talking directly; Megan was talking to some power users
		some of these projects came from those users
		James: it might be worth doing some persona development
		- Bryson has done some personas, but not necessarily the same set of users (could use his list as a starting point)
		- Can we move these personas into the public repos?  (Currently Jason guesses these would live in the Marketing Google Drive dir)
		- A slightly sharper view of users might be useful during dev
		- goal is to get user feedback as part of design process
		
		- TODO: should Jason come to roadmapping later?

* Mobile
	- They don't have any notifications yet, but it is in their MVP
	- Will use an existing API endpoint
	- Cecilia and Andrew will prep for Thursday grooming session (What is the current status of notifications?  Open questions?)
	- C and A will bring their questions back to the bigger group
	- Jason and Mithuna will talk about the design docs for notifications
	

* Individual Issues
	- Two issues from last week: Christmas Eve breakage (needs prioritization) (https://permanent.atlassian.net/browse/PER-8158)
	- Recurring donations - make sure to include in user improvement backlog list, will prioritize as part of that list

