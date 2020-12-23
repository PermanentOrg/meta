# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-12-22, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in sync on this week's goals and this sprint's status

## Outcomes
        * Review current status of some active tickets involved in recent work

## Process (Agenda)
        * Share any good news ya' got!
        * Individual Issue Items
--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
* Cecilia
* Mithuna
* Jason
* xmunoz
* James

## Notes
        * Good News
	        * Cecilia: We had a good quarterly planning day yesterday.  My neighbors are getting a puppy tomorrow :)
	        * Mithuna: went to watch holiday lights at peppermint parkway and it was super nice
	        * Jason: playing games with friends online has continued to be a comfort; and I'm feeling better!
	        * James: I think for the first time in a decade my family will all be relatively on vacation during xmas week
	        * Cristina: Ughhhhh, not a great week for good news :/
				 * Vaccine continues!
				
				
        * Individual issues
	        * Note the new time for sprint planning meetings in 2021
				*Several open issues that I need input on:
					- https://permanent.atlassian.net/browse/PER-8143 Session fixation vulnerability
					- https://permanent.atlassian.net/browse/PER-8128 Offboarding tasks
						- Mithuna will deep clone this so we have epics for Dan and Cristina
					- https://github.com/PermanentOrg/infrastructure/issues/29 Infrastructure training next week!
					  - please comment with what you want Cristina to cover
         * Also need a code review
            - https://bitbucket.org/permanent-org/task-runner/pull-requests/138
         * I would like to deploy this week!
         * Uploads
	         - pairing with Mithuna this afternoon
	         - would appreciate help in testing once we deploy to dev
					 - Cristina suggests running a Blazemeter test as part of this.  May need to modify the Blazemeter test setup to use the new endpoint(s).  (Will show Mithuna or Andrew the yaml changes necessary)
	         - deployment plan overall
					 - happy path plan: deploy to dev this week, run blazemeter next week, deploy to staging next week, and deploy to prod when everyone is ready
					- this may affect the mobile team; they're out until next year
				- Question on UI - some old copy about "out of space" is now being triggered in addition to some new messages
				- Jason, Mithuna, and Dan have a feature branch where they need to do git history cleanup
				- Share API docs from Confluence with Jason so he can look at what the mobile team is using
			- Also Jason has an old PR he is going to merge
					https://bitbucket.org/permanent-org/daemon/pull-requests/28 (thanks!)
		* Mithuna
			Share Notification : Created 3 design docs. Waiting on everyone to comment and movethese documents from draft to Approved. Also created jiras for the same. 
			- New look for the notifications with actionable items https://docs.google.com/document/d/1x8Ewbks7Lsigk6ZQGVmbZH_UqJOQboL5bCiDL84-QGg/edit#
			- Adding Share activities to the current notification feed https://docs.google.com/document/d/1-lIM5J79PaRM60pOwOjYN5iIK0jL_mFmwova2vAqeHQ/edit#
			- Unified Notification feed https://docs.google.com/document/d/1GZpF06d99IL_p2wcwlyPKfkpv4OQqYUhHAiaCLqVAZc/edit#
			Just had an issue with sentry in local, which seems to be resolved now.  
			Upload: will pair with Jason today afternoon.
			- Design doc process: more used as a way to seek feedback.  Need to set up an explicit "this is ready to start work" process
				* Cristina to review the design docs
         * I need to verify that Jason and Cristina are done.  I think they are, but hearing them say it definitively would be nice.
         * Added PER-8029 to this sprint because I think it is already being done
	         - https://permanent.atlassian.net/browse/PER-8029
         * Need to plan official offboarding (with ssh key removal and deployment)
	         - Cristina prefers to offboard both her and Dan at once so we only have to deploy that one time.
## Followup Conversations
* Mithuna
	- Created offboarding epic for Dan and Cristina https://permanent.atlassian.net/browse/PER-8144
	https://permanent.atlassian.net/browse/PER-8150
