# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-10-05, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Sprint review
    * Individual Issue Items
    * OKRs round 2

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
    * Dan Schultz
    * xmunoz
    * Jason Owen
    * Andrew Atwood
    * James Vasile
    * Mithuna

## Notes
    * Good news
        * We carved a pumpkin and roasted the pumpkin seeds
        * I got a new System76 laptop, and have been very impressed with it
        * Voting!?!
        * James: my apartment is 80% packed for my move

    * Sprint Review
        * Cristina
        * Jason
            * Decided plan is to update + snapshot the existing AMIs to fix the dual IM installations (as opposed to updating the image to use a more modern base OS / package set).  Once this is done Jason will be moving to support Cristina with the terraform work and also continuing to consoldate some of the PHP repositories.
        * Andrew
            * Looking at eliminating technical debt around mdot moving towards open sourcing and open CI
        * Mithuna
            * Working to get mysql / workbench working locally in the new vagrant setup.
            * Working with Dan on the PHP integration with the new uploader service.
        * Dan
            * Tie the uploader service with a bow (tests + documentation + deployment automation)
            * Integrate uploader service with PHP, and then ultimately trickling up to mdot.
                * Goal here is to have something close to locally demo-able in two weeks.

    * Discussion of individual issues
            * Release + notes! https://github.com/PermanentOrg/meta/wiki/Releases
            * Wordpress deployment
            * Monitoring cleanup
            * Reprocessing issues
            * v2.13 UI release, public profile changes, new Share UI
            * Cristina
                * Content freeze on wordpress needs to happen: any insight on what changes we're going to want to marketing in the coming weeks?
    
    * OKRs
        * KR 1.1 – The marketing site is decoupled from the app
            * Robert mentioned the possibility of moving to a different CMS?
        * KR 1.2 – Feature three public archives on Permanent.org
        * KR 1.3 – A design decision is made based on the results of (five or more) user 
        * KR 1.4 - Release MVP mobile apps for android and iOS.
        * KR 2.1 – Mdot is deployed via free Travis.org.
            * Open source Mdot.
                * Move repo to GitHub
                * Scrub secrets, including rotating committed keys
            * S3 Mdot deployment.
                * Move environment details into environment variables; eg API_HOST=https://dev.permanent.org
        * KR 2.2 – Robert is able to upload 100 files without any permanent system errors.
            * Uploader service deployment. (Dan)
            * Uploader service integration with PHP / MDot. (Dan + Mithuna)
            * System wide monitoring and infrastructure automation. (Cristina)
        * KR 2.3 – An external third party adds user data to our system via API.
            * ((We are recommending that this be dropped in lieu of 1.4))
