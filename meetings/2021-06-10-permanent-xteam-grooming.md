Purpose: To collaborate accross engineering and business development teams to imoprove our product and user experience

Outcomes: 
    * Engineering team knows what to work on and criteria for success
    * Business development team surfaces priorities
    * QA point people are assigned to validate improvements
    * Everyone has a bettter understanding of the issues
    
Process:
    Basically this deck: https://docs.google.com/presentation/d/150r4JC40hB3D1fi3nvPrTJam_TxTzgb7P31DZ9Zk6rE/edit?usp=sharing
    

2021-06-24 Agenda
	* issues related to organization
		* using story points and standardizing to stories
			* When you make a ticket in JIRA there's a create button
				* project Permanent
				* issue type: always choose story
			* Eng team may move or change things later, but they can decide later on their own. 
			* This allows them to assign story points – i.e. tee shirt sizes
		* deploy windows
			* set windows on the team calendar to prevent deployment conflicts
			* biz team put meetings where there moght be demos on the team calendar
			* engineering team puts their deployment windows on team calendar
			* 3 ways to follow the team calendar
				* invite yourself to events you create on team calendar
				* join the #staff-calendar channel on Slack
				* maybe: subscribe to calendar in GSuite (Google Workspace)
		* hot potato :)
			* continuing conversation about assigning QA persons and having them respond
			* There is a QA assignee field on JIRA we could use
				* Kaitlyn is bought in on Jira! let's do it
				* Let's keep a lot of the discussion of a ticket in Jira
				* Discussions in slack that result in a decision should be documented in Jira
			* who is the right person to assign to QA?
				* Kaitlyn by default?
				* we'll need to use our discretion on which things need Robert's feedback
				* Kaitlyn can do a first pass, then ask Robert for additional review
				* maybe Kaitlyn can assign Robert as a watcher on a ticket? or something similar
	* Review the cross-team grooming list
		* https://permanent.atlassian.net/issues/?jql=labels%20%3D%20%22cross-team-grooming%22
		* Zoom capability
			* KJ did some landscape analysis on adjacent platforms
			* considers this a pretty important priority because several users have mentioned it
			* Robert says he remembers there is a open sourced library that does these. Should research on that. - IIIF!
			* LOC uses: https://openseadragon.github.io/ (iiif.io might be the higher level thing?)
			* J asked what is the requirement. KJ will modify her ticket to reflect that. 
			* Prioritization - is this an epic-level task that involves more improvements to viewing/editing files by using one of these libraries?  Or just adding zoom?  Somewhere in the middle?
				* Outcome: next step is to pull the view/edit file stories together in an epic so that the eng team can assess LOE
				* Outcome: Kaitlyn will give eng a rubric of "necessary," "nice to have," "blue sky" levels
		* Batch editing metadata
			* This might be another epic level improvement
			* 
			* Can discuss about this during Roadmapping.
			* R says it is worthy. Meta we need to find the level.
			* R thinks KJ and himself need to do a pre-meeting for prioritizing. Tom  and AR TBD.
				* Split discussion into higher-level epics and individual stories that are ready to act on (K and R will split those up ahead of time)
			* 







2021-06-10 Notes

https://permanent.atlassian.net/issues/?jql=labels%20in%20(cross-team-grooming)%20and%20status%20%3D%20Open%20order%20by%20created%20DESC
	* Zoom feature is important / comes up a lot!  Kaitlyn will continue to work on some of these tickets (i.e. get more examples of how other platforms do things)

https://github.com/PermanentOrg/meta/wiki/Releases

Current release 
	* Fix the two-archives-in-two-tabs bug
		* accept current improvement
		* open 2 new issues to address QA stuff
			* https://permanent.atlassian.net/browse/PER-8388
	* Some cleanup (remove unused code)
	* Move to archive root
		* Vault: mentioned in the manifesto: https://www.permanent.org/what-we-do/manifesto/
		* Apps: let's hide this altogether for now (along with Vault)
			* open an issue to figure out move in/out of apps folders (Natalie, can you open this?)
		* Shares:
			* in theory this should be possible but there are a lot of hurdles in the way
			* exists as a separate issue already
			* not in this release
			* https://permanent.atlassian.net/browse/PER-8359
	* Invitation codes
	* Notification service dependencies (mobile)
	* Delete tokens from notification service (mobile)
	* Upload service dependencies (mobile?)
	* Improved push notifications (to prod) (mobile)
	* Take token from etherpad (gftw)

Outcome: yes, we'll release!  Pending another invitation code test on staging and removing Apps/Vault from the move/copy modal.


