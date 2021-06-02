# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-06-01, 11:15am CT
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
	* Cecilia
	* Mithuna
	* Jason

## Notes
                        
* Good News
	* I'm fully vaccinated now! And was able to play board games with friends🎉 
	* Took our guests around Austin and revisted many scenic locations again..
	* I fell in the lake!

* Open PRs
        * GitHub: https://github.com/pulls?q=is%3Aopen+is%3Apr+archived%3Afalse+user%3APermanentOrg+
        * BitBucket: https://bitbucket.org/dashboard/pullrequests?section=all&workspace=permanent-org
        
* Projects
	* Question about device token registration failure
		* See conversation between Mithuna and Vlad here: https://permanent-org.slack.com/archives/C01AK4233TN/p1622235341047100
		* Mithuna's device isn't being registered
		* We log the notification-service to systemd; Jason will find the exact journalctl command for Mithuna (and Mithuna will document)
		* Note that if the logs aren't showing up we may want to use a higher logging level.  We'll do that as a one-off for now.
	* Plan for editable tags change
		* name-archive-type should be the new three-way uniqueness test (PER-8341)
		* Cecilia suggests that archive ID be nullable, to account for potential future global tags.  Also suggest we keep the existing tags and make new versions of each of them: e.g. "summer" and "summer belonging to <archiveId>" will both exist
		* Mithuna will do some research into a migration solution but not spend more than a few hours on it: see PER-8300
			* https://permanent.atlassian.net/browse/PER-8300
	* GFTW
		* Jason to clean up his local work for the plugin UI
			* upgrade dependencies on plugin
			* move sdk connection into plugin
			* review PRs
			* get changes onto pad.staging
		* Cecilia to clean up the node-sdk PR
	* Cecilia to share Amberly and Amy's recent presentations with Mithuna

