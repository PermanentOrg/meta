# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-09-08, 1pm CT

Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
* Review current status of some active tickets involved in recent work
* Review of sprint goals, particularly what's up for open sourcing (proposed by Karl)

## Process (Agenda)
* Proposed item: Good news!
    * I, like many of us currently, have been having a rough go of it. I'd like to start each of our meetings with some good news from whoever has any. +200
* Individual issue areas
* System-monitor alerts processes
* How far are we from knowing that uploads are working?  (Karl)
* Etherpad / Confluence / Github or some other public place

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.

* Cristina
* James Vasile, james@opentechstrategies.com
* Jason Owen <jasonaowen@opentechstrategies.com>
* Karl Fogel <oh come on you know my email address let's not be silly>
* Andrew Atwood aatwood@permanent.org
* Dan Schultz (dan@opentechstrategies.com)

## Notes
* Good news
    * Karl ate a LOT OF CHEESE and didn't use any computing power.
    * Dan's family got a patio installed outside!  But they don't have furniture, so they're just playing giant chess games using neighborhood kids as pieces.
    * Cristina's chickens are still alive.  "Pretty stoked on that."
    * Low-quality air near Jason seems to have blown away last night.
    * Andrew got outdoor time

* System-monitor alerts processes
    * On Monday, Robert uploaded a bunch of stuff and got a fair number of failures (17 out of 430), and some of the data was lost (at least, not visible to the user, though the data was in fact just stuck in the pipeline and Andrew was later able to push it through).  This is a known problem, not a surprise.  Still, it was a poor enough experience that Robert even toyed with the idea of shutting off the upload functionality until it's fixed.
    * https://permanent-org.slack.com/archives/GUW9GHS4V/p1599587659019300?thread_ts=1599587288.013600&cid=GUW9GHS4V
    * Andrew is owning this right now, and it's a lot.  He and Dan will discuss what the right policy should be, and document it.

* Discussion of individual issues (Led by Cristina)

    We're in backlog of Sprint 138 right now, w/ Sprint 139 starting:

    Issue bucketing went by too fast for Karl to capture all of it, but it's kind of silly to put those details in these notes anyway -- it's all already captured in the issue tracker.

    A bunch of upload-related issues were assigned to Dan, who will handle them as he thinks best -- might mean closing them and making better issues.

    * Cristina has 4 PRs for operations repository open.  They do things like remove secret keys, add documentation, add license, etc.  Once they're merged, we can open source that repository!  See details in "Decisions" section.
    * Andrew: No new features, no new backend stuff, just straightforward improvements/enhancements/bugfixes going out this week.  Likely won't need to dip into backlog -- there's enough to do in 139.
        * Finishing up features for v2.12 as defined here: https://permanent.atlassian.net/wiki/spaces/REL/pages/620920833/New+UI+Release+Definitions
    * Jason: Fixing uploads is highest priority.  This will involve looking at Mithuna's WIP and shepherding her PRs through, then continuing from there.
    * Dan: (Karl missed some stuff here because reasons) Evaluate Mithuna's file-uploads architecture doc and build on it.  Look at reorganizing code/repositories/modularity.

* Review and prioritization of current backlog (from Epic view)
In order of priority, from highest priority to lowest:
    * Troubleshooting upload process is highest priority
    * File deletion
    * Open source
    * Automated Env Provisioning (Cristina)
    * Automated Integration Testing (Cristina)
    * Public API is on Dan's mind, even though he may not write code for it in this sprint
    * Full Responsive Web App (7537): Andrew working on

* Etherpad / Confluence / Github or some other public place
    * Etherpad->GitHub.  See "Decisions" section for details.

## Decisions
* Dan will be the Backlog Owner.

* Open sourcing the operations repository this week!  Cristina will get the remaining 4 PRs merged and push the repository (just tip, not fully history) to GitHub w/o a license; James will take care of adding AGPL-3.0 and related verbiage right after Cristina does that.

* We'll take real-time notes collaboratively in Etherpad, and then transfer the notes to a publicly version-controlled location (e.g., either a GitHub repository or a GitHub repository's wiki (which, of course, is also a GitHub repository, and why it's not wiki repositories all the way down I'll never know -- it's a huge missed opportunity on GitHub's part)).  Dan will transfer these notes, and perhaps previously Etherpadded notes, to the appropriate place.  Dan, just FYI, some examples from other OTS projects: https://github.com/OpenTechStrategies/torque/wiki/Meeting-Notes and https://github.com/redcross/arcdata/wiki/Meeting-Notes .
