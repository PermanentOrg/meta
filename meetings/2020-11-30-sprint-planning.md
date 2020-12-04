# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-11-30, 1pm CT
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
    * Dan
    * xmunoz
    * Jason
    * Cecilia
    * Mithuna
    * Karl
    * Andrew

## Notes
    * Good News
        * New county restrictions on traveling/quaratining in the county to stem pandemic spread, hope it works!
            * Lupini bean success!
                * if you die from lupini beans, you die in real life
        * Thanksgiving worked out -- had turkey flavored candy corn.  Would not recommend.
        * Cecilia is in the house!  (Note: this is not written in Cecilia's color.)
            * Okay, if we need non-work-related good news, then: my girlfriend has recovered from COVID-19 and now has magical non-contagiousness & immunity superpowers.
        * Successful holiday! First pure sourdough bread! Crusty bread!<3🔥
        * Onboarding epic looks super helpful - thanks Christina!
        * Moved into my new home
            * W00t!  :congratulations-emoji:  !

    * Sprint Review (add your notes)
        * Done / Doing / Next
        * Andrew
            * Done:
                * Changed the url redirect so it now just uses /app (not mobile only)
                * A few other bugs got patched up as well, including a pdf fix which was a quick two-day turnaround for a user!
                * Node SDK has been used in production by a third party (this seems like a pretty big deal!)
            * Doing / Next:
                * Broken facebook connector? https://permanent.atlassian.net/browse/PER-8036
                    * Ahh yes, smart
                * move mdot to GitHub (open source) - Christina, Jason, either have or will write issues for this
                    * ponder a new name!!!
        * Cecilia: expects to be doing onboarding stuff for the next few days
            * Next: archive some GitHub repos, set up error review weekly, remove/rename old pledge code
        * Cristina
        (Note: Cristina has no JIRA tickets right now -- everything is in GitHub)
            * Done
                * Crushed it!
                * Fixed up an issue where reprocessing would happen forever and ever and ever and ever (files would be reprocessed without progress).  Correcting this problem has really improved user errors.  Still, this is a short-term not a long-term fix.  Drew Cecilia's attention to the question of how to prioritize data integrity and unprocessed or partially-processed files.
                * Sleeps now happen for a full second at minimum.  This avoids a lot of race conditions.  (But Jason asks: hmm, why are we sleeping at all?  Cristina agrees that needing to sleep at all is an antipattern and should be addressed.)
                * Note lots of places where exceptions are caught but not logged / nothing happens with them
            * Doing / Next:
                * Rolling out new staging environment with packer/terraform and prod-like autoscaling
        * Jason
            * Done: progress on uploads: front-end refactoring, pairing (mostly with Dan) on backend
                * First endpoint done/merged, second one is close
            * Doing/next: finish(!?) uploads
        * Dan
            * Done: cleaned up and merged in some of Mithuna's PHP upload PRs, we now have the first (of two) new endpoints merged. One more PHP PR to go.
                * Note: we made a decision around temporary "unprocessed" folder in the upload bucket.
            * Doing / Next: Reviewing Jason's mdot PR(s). Finish the second PHP endpoint with Mithuna. Cecilia handoff + onboarding. DB credential rotation. Writing a blog post on behalf of the team about our upload adventures (anybody who wants to join in and / or co-author is welcome to it!).
        * Mithuna
            * Done: Endpoint which generates the s3 signed URL is merged
            * Done/next: The second endpoint which creates the record and other table entries is almost done. Last small changes and should be good to go.
            * Next: Work on Notifications changes. Right now notifications are archive based. Need to change that to account.
            * Add Share notifications to the notification activities.

    * OKRs / high-level goals:
        * Get mdot open sourced and on GitHub in this next sprint.
            * https://permanent.atlassian.net/browse/PER-7875
            * Jason asks: what are the blockers?  Andrew said not much; did a review earlier and there were just some API keys, nothing major.
            * Dan: "The spirit of the OKR is that we get to a point where with mdot you push and it gets merged to the right place and then it goes live. [...]  You don't have to do [anything manual]."
            * Priority relative to other stuff discussed today: 1) open source mdot, then 2) fix the Facebook connector, then 3) make the CI described in the previous bullet point work.

    * Individual issues
        * Upload monitor- whose reposibility to triage?
            * https://permanent.atlassian.net/browse/PER-7971 - Cecilia
        * Archive some archiveable repositories in the GitHub org -- Cecilia will do, because that will ensure that she gets the necessary permissions on GitHub.
        * clean up pledge action - https://permanent.atlassian.net/browse/PER-8021 +1 cecilia volunteers
        * Security review of new architecture - Dan is going to schedule a meeting
        * Data validation of the functional test - Assign to cecilia
        * Documenting the new Upload process
