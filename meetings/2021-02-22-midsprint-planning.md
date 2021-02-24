# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2021-02-22, 11am CT
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
- Andrew 
- Cecilia
- Mithuna
- Jason


## Notes
        * Good News
	        - My dad got his first vaccine appointment!
				- No more snow 
				- Sunshine ☀️
	
        * Individual Issues
	        - Andrew: documentation
	        - Deploy today: family search notifications and new folder, verification codes, case-insensitive tags (db change), download with original filename (whoo!)
				 - Jason idea: schedule a meeting or get some issues from Andrew about plans for the web-app, ideas for next steps, half-done things :)
				- Jason
					- GFTW
					- Notifications: prototyping db migration tools
					- Schema inconsistency - waiting on Cecilia for review, all to run db migrations locally
				- Cecilia: to reprioritize things for March!  Upload cleanup, Internet Archive, metadata
        * Mithuna 
	        - Account deletion unit test. We had 2 ideas I think may be creating an account before deletion might be the easiest. thoughts?
		        - Possibly following the functional test - i.e. curl the "create account" endpoint so that it fills in the necessary tables
		
  -8160 - moved to  the next sprint
		
		
## Followup
- Cecilia (and Mithuna?) to click through the deploy steps

	* Merge PRs in 
		* Api - DONE
		* Library - DONE
		* Web-app - DONE
	* Change dev database with new collation - DONE
		* SHOW CREATE TABLE tag; -- check what it looks like
		* ALTER TABLE tag MODIFY name VARCHAR(100) CHARACTER SET utf8 COLLATE utf8_bin;
	* Code deploy to dev - DONE
	* (I clicked through the new features here, too, to make sure they worked)
	* Functional test on dev - DONE
	* 
	* Merge api and library repos up to staging - DONE
	* Change staging db - DONE
	* Code deploy to staging - DONE
	* Functional test on staging
	* 
	* Merge api and library repos up to prod - DONE
	* Change prod db - DONE
	* Code deploy to prod - DONE
	* Functional test on prod
	* 
	* Write up release notes
