# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning 2021-03-01, 11am CT Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

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
- Mithuna
- Jason

## Notes
- Cecilia focused on hiring, SDK, metadata changes (moving a lot of tickets out of this sprint)
- Deployment(s)
	- Mithuna's slack monitoring and Andrew's Internet Archive changes are in dev now
	- Need to merge a library PR of Andrew's first: https://bitbucket.org/permanent-org/library/pull-requests/134
	- Test new things on dev, then promote to staging
	- Then Jason will update backend and promote through the environments
- Local schema
	https://bitbucket.org/permanent-org/docker/pull-requests/17/make-local-ci-schema-consistent-with-dev
	Mithuna to run in vagrant
- Notifications tickets are in GitHub; Jason and Mithuna planning to pair
- GFTW:
	- New endpoint: validate a shared secret, add storage to the appropriate table (based on the fetched file)
	- Jason will update the ticket
- Mithuna is going to focus on notifications, then deletion, and emails.  She will split up the "load test" ticket into smaller ones so that we can make some progress.
- Deletion being broken
	- The test for deleting an account *should* be running in our pipeline.  Why didn't it alert us that deletion is failing?
		Is this working correctly? https://bitbucket.org/permanent-org/api/src/c362e45a8aabe99a34cd08442ec50ee77a5517ba/tests/controller/account/AccountControllerTest.php#lines-493
	- Mithuna will look at this: https://permanent.atlassian.net/browse/PER-8285 and we hope also fix the corresponding test!
	
- Open sourcing mdot
	- Final blocker will be the Google Maps API key, but in the meantime we need to rotate other keys which are in the epic.  Those tickets need to be assigned to a sprint so that we can open source the web-app repo!
	
- Upcoming conferences? APPO (Association of Professional Photo Organizers) in June, possibly

-Google maps API key(verify before sharing with Robert)
	https://developers.google.com/maps/documentation/maps-static/get-api-key

# Good news
- Oregon vaccines will be available to anyone who wants it no later than July 1!
- My neighbor gave me a loaf of sourdough! <3
