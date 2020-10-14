# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-10-12, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
    * Review current status of some active tickets involved in recent work

## Process (Agenda)
    * Share any good news ya' got!
    * Individual Issue Items

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
    * Dan Schultz -- dan@opentechstrategies.com
    * Jason Owen
    * Andrew Atwood -- aatwood@permanent.org
    * Mithuna
    * Karl Fogel -- kfogel@itsnoteasytomakeupanewdomainnameeveryweek.com

Note: Cristina took the day off for Indigenous People's Day.

## Notes

    Today is a mid-sprint catch-up.

    * Good news
        * Karl's choir met for the first time in 8 months!  https://golosa.org/, just to provide receipts.
        * Lyla had a birthday!
        * Enjoyed time with extended family.
        * We should play "Among Us"
            * key term to know: "sus" -- suspect

    * Discussion of individual issues
            * Are we ready to integrate with the new direct-S3-upload API -- i.e., the get-a-file-upload-destination API?
                * Dan's aiming to have the new service module ready, and integrated into build system, by mid-tomorrow (mid-morrow's eve)
                * Caller integration work is starting now and is expected to take until the end of October.  It includes changing mdot, upgrading PHP, the whole kit & kaboodle.
                * Epic for this https://permanent.atlassian.net/browse/PER-8024
                * Some in-meeting discussion between Jason and Dan about exactly how the integration into the build system will happen.  Initial implementation will be to just use a small/micro EC2 instance, with containerization to perhaps come later if we decide it's worth doing.
            * Jason is still working on the ImageMagick issue.  Hasn't found any package repositories that will give us what we need, so he may resort to compiling from source.  An alternative is to upgrade our OS so that we get a recent enough ImageMagick, but that's a much bigger ball of wax; for now, Jason would prefer to solve this in a more well-bounded way.
                * Andrew: What if we spun up an independent image conversion service, calleable via command line, so that upgrading/managing that would be an isolated thing?  Discussion ensued about our long-term image transformation needs and treating that as a service, perhaps an outsourced one.
            * Mithuna: Writing tests for some work done recently (has call with Jason today to see why those tests are currently failing).  Other than that is available to work on whatever is most important; will confer with Dan.
            * Andrew: No blockers.  Upgrading deps so NPM doesn't yell at us anymore.
                * Re micro-SDK for TheirStory: Andrew will want to pick someone's brains about how best to set up a Node-based project for publication.  Dan says he can help, and mentioned semver, publishing changelogs with the package, documentation, etc.
    
    * OKRs
            * Dan, I'll let you summarize this decision (re mobile & API) here or below
            * Decision is: We're going to take off the API KR and replace it with the mobile prototype KR. +1

