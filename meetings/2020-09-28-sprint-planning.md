# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-09-28, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
Review current status of some active tickets involved in recent work

## Process (Agenda)
Share any good news ya' got!
Individual Issues
Release Notes on Github: https://github.com/PermanentOrg/meta/wiki
Lets pick some OKRs!

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
Dan Schultz <dan@opentechstrategies.com>
Andrew <aatwood@permanent.org>
Xmunoz
Mithuna <mkrishna@permanent.org>
Karl Fogel <kfogel@synergistically-iterate-plug-and-play-testing-procedures.com>
(My editor can generate these things!  Ask me how!)

## Notes
- Good news
  - Dan: Mother in law retired last week after 52 years of working!
  - Cristina: I have harvested so many tomatoes this summer, that I haven’t had to buy any
  - Jason: Sourdough starter ftw

- Discussion of individual issues
    - Dan
        - Strict linting rules are a great way to drink from a firehose!
        - Intent is to have the uploader service demo-ready for Friday that is generating fileDestinationUrls to any principal with {the configured secret} (authentication TBD based on discussion in GitHub).
        - Plan is to integrate it with existing code the week after.
        - Jason thinks auth can be simpler than he thinks Dan thinks it is, and would like to chat with Dan about it. (though to be clear… I agree auth can be pretty simple right now!!)
    - Cristina
        - Deprecate the files/ repository
        - It’s a grab-bag of random files.  Some are important configuration files.  Some are random images and whatnot.  Some are icons used by the application.  There is no conceptual unity at all.  This repository needs to go away, and its contents all moved to various appropriate places.
        - Cristina anticipates this being 5-6 PRs.
        - Completely remove web-client/ from the current images
            - This is the predecessor to mdot.  The only people who get the old web-client UI now are those who opted out of the new UI (prior to the removal of the opt-out option).  So taking this step implies identifying and upgrading those straggler people to the new UI.  Andrew thinks it’s not a huge lift; will check the total numbers, but doesn’t think this is a huge concern.
            - We want to remove it completely so we can make sure nothing else breaks.
          - Investigate and write config management for monitoring
              - Not yet sure how monitoring is instrumented, but need to learn what monitoring is in place & see what needs to be cleaned up and/or tweaked.  Will work with Mithuna on this.  AND MITHUNA IS BACK.  Just had to say that again.
          - Triage and mitigate ODT and and other document file thumbnail generation failures on devenv
              - Would like to pair with someone to find out why they’re failing.
          - Things people need from me: I’m getting a lot of notifications about activity in Github. If you need input or design feedback, please me ping! For big-picture design questions, I prefer talking to writing things in Github Issues.
    - Andrew
        - No blockers -- ready to roll and rock!  (Wait, is that the expression?  -Karl)
    - Mithuna
        - Will chat with Dan to set priorities
        - Pick back up issue with invite codes
        - Getting back up to speed in general
    - Jason
        - Got some cleanup done
            - Finish shepherding trio of PRs
        - Continue to review pull requests
            - Includes above-mentioned auth conversation with Dan
        - Still have more digging to do to diagnose reprocessing errors

- OKR discussion (see Google Doc)
    - Cristina high level thoughts:
        - We have 4.5 people doing engineering work; lets try to target two (2) KRs!
    - What is important!
        - Dev environment work
            - “Anyone on the team should be able to ___”
            - Database stuff was not included last quarter; will it be included this quarter?
                - No it will not.  There is a bit of DB work to do but we won’t be upgrading mysql.
            - Something related to Docker?
            - Something related to continuous integration / continuous deployment?
        - Consolidate PHP repositories into a single repository.
        - Change the way mdot is deployed so that it is built by travis and published to S3 / a CDN. (Objective 2)
            - Broad concept here is: redesigning the deployment workflow.
            - Remove the need for slack command to deployment.
            - Open sourcing mdot
        - ++ Proposed KR: Deploy mdot using free Travis.org
        - ++ + Uploads
            - KR rooted in architecture direction?
            - KR rooted in user story / user experience?
                - E.g. “Robert is able to upload 100 files without any system errors.”
                - “All file entries in the database (or a very high %?) have a file accessible in S3” ← (are there VALID situations where an entry would NOT result in a file?) (not in the new architecture I don’t think..?)
        - API endpoints / Partner integration
            - Data (what data) is inserted into our system via an external service. (Their Story)
        - KR related to monitoring
        - + Full introspectability into the production application - xmunoz
            - Monitoring on PHP application, and uploader.
            - Machine-level monitoring
