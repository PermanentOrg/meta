# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-03-23, 11am CT
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
- Mithuna 
- Cecilia
- Jason

## Notes
			
* Good News
- My first daffodil bloomed today. 
- I had a good weekend!
- 


* Open PRs
https://github.com/pulls?q=is%3Aopen+is%3Apr++archived%3Afalse+user%3APermanentOrg+

- https://bitbucket.org/permanent-org/docker/pull-requests/20
	Assigned to me; I will do
- https://bitbucket.org/permanent-org/back-end/pull-requests/1
	Has broken tests; one of us need to fix. We should either fix or close.
	Do we actually want this? After some discussion, yes probably; Jason will clean up.
- https://bitbucket.org/permanent-org/back-end/pull-requests/3
	Will work on the changes Cecilia mentioned 
- https://github.com/PermanentOrg/node-sdk/pull/15
	Cecilia needs to do the things that Jason asked for in his review!
- https://github.com/PermanentOrg/upload-service/pull/26
	Cecilia will review (Jason suggests commit-by-commit)
- https://github.com/PermanentOrg/infrastructure/pull/38
	None of us really remember this; Cecilia will figure out what this is supposed to be doing and why, and then decide to rebase & resolve conflicts or close it
- https://github.com/PermanentOrg/infrastructure/pull/39
	Cecilia closed in the expectation that I will reopen in future when autoscaling becomes a priority again.
- https://github.com/PermanentOrg/infrastructure/pull/46
	Made the changes requested. waiting for Jason's rereview.
	I will look!
- https://github.com/PermanentOrg/notification-service/pull/4
	Mithuna has made the changes Jason suggested; Jason needs to re-review, and Cecilia can also review
- https://github.com/PermanentOrg/notification-service/pull/13
	Mithuna will review 
- https://github.com/PermanentOrg/devenv/pull/23
	closed
- https://github.com/PermanentOrg/functional-test/pull/7
	Mithuna will make requested changes and we can merge!
- https://bitbucket.org/permanent-org/back-end/pull-requests/11
	Mithuna is still working on
- https://bitbucket.org/permanent-org/email/pull-requests/32
	Mithuna to review (in the past Permanent has not deleted templates from Mandrill; Mithuna will ask Robert about this policy)
- https://bitbucket.org/permanent-org/back-end/pull-requests/7
	Jason will fix to not break the iOS app, but still remove almost all the back-end code


* Individual Issues
- Cecilia: metadata, GftW upload, feedback on metadata-as-tags, plus non-sprint-work (TheirStory, quarterly planning, WordPress contractor), mobile team found latlong type issue
- Mithuna: Need some project assinments on push notifications. 
	- Top priority: getting it deployed!  (Open PR for that in infra repo, #46, see above)
	- notification-service build via github action; see upload-service
		https://github.com/PermanentOrg/notification-service/issues/20
	- https://github.com/PermanentOrg/notification-service/issues/17
- Jason:
	- pending PRs
		- infrastructure#46
		- back-end#7
		- docker#20
		- back-end#1
	- data format for mobile team - I will make first draft, and put in #public-mobile-dev slack for C & M to review
	- New notification service databases are up but need to be connected to build/deploy pipeline
	- GFTW: thinkin' bout authentication (also very relevant for upcoming TheirStory updates)
	- upload legacy mobile apps to github
- https://github.com/PermanentOrg/notification-service/milestone/1
	mobile team needs: data format, list of notifications
	our current list: one-week-later user feedback; 10-days-later upload reminder
		these are very simple, maybe also one that also needs some context?
		share notification - Mithuna's Flower Archive shared the lily picture with Jason's Bread archive (i.e. NOT a collaboration request / invitation to an archive)
		try to have these (specifically the data formats) by Thursday morning to hand off to the mobile team
