# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-11-16, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Sprint Review
    * Individual Issue Items

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
    * xmunoz
    * kfogel
    * mkrishna
    * aatwood
    * Dan
    * Jason

## Notes
    * Good News
        * Brought a new home :) 
        * KIMCHI IS DELICIOUS
        * Takin' care of a dog; turns out to be fun.
        * Dan: I decided to relive my childhood and put together this castle: https://brickset.com/sets/6090-1/Royal-Knight-s-Castle
        * 
    * Sprint Review (add your notes)
        * Done / Doing / Next
        * Cristina:
            * Done
                * did a deep dive into what's going on in our machines, which resulted in a fancy spreadsheet that shows what is / isn't redundant, as well as a few items to remove from un-necessary environments.
                * AWS credential review and cleanup with Andrew
            * In process / Next
                * Splitting up task runner
            * Other Notes
                * Planning to close out the wordpress content sync tasks; thinking will be that we can manually move any new blog posts if they happen in the transition time, re-examine the resubmit-unprocessed job and either turn off or tweak to make more effective
        * Mithuna:
            * Done
                * API endpoint that interacts with the upload-service PR is open and feedback has been addressed.
                * Metadata pipeline / schema work which is being taken on by Andrew.
            * In Progress / Next
                * Working on the second endpoint, but need clarity on what we want that to do.
        * Dan: 
            * (SO CLOSE TO) Done
                * Spreadsheet outlining what's been worked on the past few months.
                * Sentry PR for upload-service is open; related infra PR is incoming.
        * Andrew:
            * working with Mithuna on metadata for partner
            * Integration with another partner that uses CLI tool
        * Jason
            * Done:
                * vagrant bug
                * router cleanup
                * upload to S3
            * Next:
                * upload to S3
                * pairing with Mithuna on second API?

    * Individual issues
        * Cristina: Deep clone for onboarding had unexpected behavior, did you use this base epic? https://permanent.atlassian.net/browse/PER-7699
        * Mithuna: Second upload API endpoint responsibilities.
            * We are doing the downloading to the upload folder so that transformations function in roughly the same way.
            * We'll be careful to download from S3 as part of the processing task, and not as part of the API request handling
        * Dan : Sentry + infrastructure
            * where should environment-specific configuration live, in infrastructure as environment variables or in the compiled code? Cristina's first impulse was the latter, but after further discussion we decided to go with the former
            * https://github.com/PermanentOrg/infrastructure/issues/9
