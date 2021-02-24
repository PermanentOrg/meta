# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning 2021-02-08, 11am CT Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

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
	* Mithuna
	* Cecilia
	* Jason

## Notes

* Good News
	* Cecilia: Cold outside, warm inside!
	* Mithuna : Furniture makeover obsessions. 
	* Jason: traded bread for lasagna
	* Andrew: new lights (pics in slack)

* Sprint Review (add your notes)
	* Uploads -> prod, wow!!
	* Open sourcing web-app; any blockers left?
		* none!
	* Prep for next release - which tickets?
		* Upload cleanup epic: https://permanent.atlassian.net/browse/PER-8252
			* We will add more 
		* FamilySearch modals
		* CD vs release trains?
			* we have some specific events that we want to freeze around
			* maybe more conversations later
	* Probably need to drop some tickets from this sprint
		* Cecilia dropped: PER-8123, PER-8173, PER-8174, PER-8168, PER-8096
		* Andrew dropped: PER-8217
		* Mithuna : PER-8142, PER-8162
	* 
	* Push notifications?
		* Question: What about authn/authz to external services?
			* Does Firebase handle this for us? https://firebase.google.com/products/cloud-messaging
			* Jason : Double check with mobile team that firebase is fine. Cecilia will check with them next week (this Wednesday, 10 Feb)
	* Notifications this week:
		* Finding a good branching point from upload-service
		* Setting up a new database in PostgreSQL


	* Rolling back the upload deploy to prod
		* Apply an older image (which?)
		* How do we do this in Terraform?
		* Practice in dev first!

* OKRs

* Individual Issues
	* https://permanent.atlassian.net/browse/PER-8117 (unify PHP repositories)
		* Keeping this in BitBucket for now, we can move to GitHub as a separate task
		* 
