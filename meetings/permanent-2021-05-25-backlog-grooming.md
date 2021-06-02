# PERMANENT LEGACY FOUNDATION – Permanent.org
Backlog grooming 2021-05-25
Hosted on Google Meet at https://meet.google.com/mkr-agtf-iay

## Purpose:
Engineering team reviews old tickets

## Outcome: 
	* The tickets in the engineering backlog have enough detail and value to be assigned in a subsequent sprint

## Process
	1. ~20 minutes per person's set of tickets
	2. Start with oldest tickets, move forward
	3. Break after first two sets

## Preparation
Review issues before meeting:
	* 
	* Mithuna: oldest ones! https://permanent.atlassian.net/issues/?jql=status%20!%3D%20Done%20AND%20(sprint%20is%20EMPTY)%20AND%20project%20%3D%20Permanent%20AND%20key%20%3C%3D%20PER-7820%20ORDER%20BY%20createdDate%20asc
		* We closed most of these since they are part of a "Productionize the API" epic for the public api project that is no longer happening
	* Jason: medium old https://permanent.atlassian.net/issues/?jql=status%20!%3D%20Done%20AND%20(sprint%20is%20EMPTY)%20AND%20project%20%3D%20Permanent%20AND%20(key%20%3E%20PER-7820%20and%20key%20%3C%20PER-8120)%20ORDER%20BY%20createdDate%20asc
		* Jason intends to make a processing epic and put several of his tickets into it, since we know that's on the roadmap
	* Cecilia: medium new https://permanent.atlassian.net/issues/?jql=status%20!%3D%20Done%20AND%20(sprint%20is%20EMPTY)%20AND%20project%20%3D%20Permanent%20AND%20(key%20%3E%20PER-8120%20and%20key%20%3C%20PER-8250)%20ORDER%20BY%20createdDate%20asc
		* Moved some of these to epics so they are more easily findable
		* New website epic: https://permanent.atlassian.net/browse/PER-8215
		* To do: make a "synchronization bugs" epic
	* Natalie: most recent ones!  https://permanent.atlassian.net/issues/?jql=status%20!%3D%20Done%20AND%20(sprint%20is%20EMPTY)%20AND%20project%20%3D%20Permanent%20AND%20key%20%3E%3DPER-8250%20ORDER%20BY%20createdDate (all not done and not in a sprint more recent than PER-8250)
		* Actually should be more like this, to avoid all the ones that people have made in the last day https://permanent.atlassian.net/issues/?jql=status%20!%3D%20Done%20AND%20(sprint%20is%20EMPTY)%20AND%20project%20%3D%20Permanent%20AND%20key%20%3E%3DPER-8250%20AND%20createdDate%20%3C%20%272021-05-21%27%20ORDER%20BY%20createdDate

## Discussion
For each ticket: 
	1. Do we understand what it is?
	2. Does it urgently need to be fixed?
	3. Can it be closed?
	4. Is it reproduceable?
	5. Is it associated with the correct epic, if one exists?

## Individual tickets
	* https://permanent.atlassian.net/browse/PER-7628 - we still want these tests; leaving open
	* https://permanent.atlassian.net/browse/PER-7708 - the "public API" repo was abandoned, and all of these issues can be closed as wontfix
	* https://permanent.atlassian.net/browse/PER-7657 - this is still work we want to do
	* https://permanent.atlassian.net/browse/PER-8143 got partially split into a sub-ticket; Mithuna will find and link that other ticket
	* https://permanent.atlassian.net/browse/PER-8170 Cecilia will look at more closely, and split into separate tickets
	* https://permanent.atlassian.net/browse/PER-8180 Cecilia will make a sync epic
	* https://permanent.atlassian.net/browse/PER-8242 add to sync; there might be a duplicate ticket Mithuna created
	* https://permanent.atlassian.net/browse/PER-8260 Jason will add more detail
	* https://permanent.atlassian.net/browse/PER-8284 Cecilia will add more detail / clean up conflicts in description
	* https://permanent.atlassian.net/browse/PER-8289 Jason will add to processing epic
	* https://permanent.atlassian.net/browse/PER-8292 Jason will add to processing epic

For next time:
	* https://github.com/issues?q=is%3Aopen+is%3Aissue+archived%3Afalse+user%3APermanentOrg+
