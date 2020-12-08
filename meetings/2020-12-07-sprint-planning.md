# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-12-07, 1pm CT
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
- xmunoz
- Cecilia
- Andrew
- Jason
- Dan

## Notes
	* Good News
		* Started working out again and taking iron supplements, both have had a noticeable impact on my vigor
			* gotta give it up for vigor
		* First batches of the vaccine shipping out soon!
			* https://www.nytimes.com/interactive/2020/12/03/opinion/covid-19-vaccine-timeline.html
		* Walked on a frozen lake and made sticky toffee pudding
		* Really nice weather in the afternoons this week
		* Christmas Tree decorated. Organized a baby shower. 
		* Finished Brandon Sanderson's Warbreaker this weekend; it is a very good book
			* released under creative commons?? (According to Google) l337! yeah! he posted it chapter-by-chapter as he wrote it
		* I'm getting a rowing machine!!  Which I think means I'm healthy now?DEEZ GUNS

	* Individual issues
		* Mithuna is focused on upload endpoint (that's her main task)
		* Mithuna is also working on a design doc for the notifications
		* Dan probably will not be able to do PER-8096 before Friday 
			* Cristina might be able to pick this up if the prod rollout goes smoothly!
			* (Focused on upload PHP pairing!) :)
		* Cristina is mostly working in GitHub issues
			* Autoscaling is going to be put aside for now
			* A thing to do instead might be to look at server metrics to see what size the machines should be, etc
			* Wordpress is also a blocker for autoscaling (because it is edited locally)
		* Cristina hopes to finish image creation tomorrow
			* Will be working on deployment doc with Andrew and anyone else who wants to observe
		* Blazemeter might be blocked
		* Production code freeze: should do a deploy today (pre-freeze)
			* Wednesday will start the freeze, when xmunoz pushes to staging
		* Jason is mostly on uploads, with some code review
			* mdot side of uploads!  PR is open for Dan, hope to merge today for Andrew (refactoring)
			* J has some local work that is semi-blocked on the second endpoint (needs just the design to be done)
		* Monitoring:
			* "total error" in the weekly report - why did those fail?
			* And then a few failed on Sunday
			* Cecilia and Mithuna to pair on those
		* Andrew has some pre-freeze changes:
			* SQL strict mode fixes - handling dates that are not formatted properly
			* Mobile team needs to be able to copy a file in the same location
		* Andrew also wants to make some node-sdk changes for TheirStory
		* m-dot to GitHub! splitting the two projects out into separate repos
			* environment file 
				* https://permanent.atlassian.net/browse/PER-8110
				* https://bitbucket.org/permanent-org/mdot/src/dev/src/environments/environment.prod.ts
		* Cecilia and Dan will have a followup / hand off conversation in the next couple days
		* Dan to review a node-sdk PR https://github.com/PermanentOrg/node-sdk/pull/11
		* Congratulations Dan on getting a PR into the Amazon sdk!
			* https://github.com/aws/aws-sdk-js/issues/3486#event-4074530054
		* New node uploader will be deployed on new prod (for consistency with other environments)
		* Mobile team is using an endpoint for uploads that we are not familiar with.  It needs to stay up!
			* Possibly using an AJAX version of a known endpoint (instead of the websocket that mdot uses)
			* Andrew will let us know what they're using so we don't accidentally turn it off
		* 


## Followup Conversations
	* remaining upload work (Dan & Jason post-call)
		* rollback on error (delete from s3; delete created db objects)
		* download file for local processing in task-runner
		* move object in s3 from unprocessed to expected location
			* remove code from task-runner to upload file to s3
		* create autodeletion bucket policy

