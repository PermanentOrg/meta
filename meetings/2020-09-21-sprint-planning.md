# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-09-21, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
- Review current status of some active tickets involved in recent work


## Process (Agenda)
- Share any good news ya' got!
- Release Notes on Github: https://github.com/PermanentOrg/meta/wiki
- New epic for migration bugs that require follow-up, and also general bugs that I've noticed along the way


--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
    * Karl Fogel <kfogel@"".com>  ("Open Tech Strategies: We're the '' in '.com'!")
    * xmunoz <xmunoz@xmunoz.xmunoz> :P
    * Dan Schultz <dan@opentechstrategies.com>
    * Andrew Atwood <aatwood@permanent.org>
    * Jason Owen <jasonaowen@opentechstrategies.com>

## Notes
* Good news
    * Karl has a cool and ancient light on the ceiling!
        * "Cool and ancient light."  I suddenly feel as if I'm trapped in a W. B. Yeats poem.
    * Jason saw sunlight. And it wasn't even a little bit orange.
    * Cristina's chicken is laying eggs again!

+ Higher level stuff
    + Cristina has identified some performance and security issues.  E.g., deleted some legacy firewall rules that allowed access from random IPs.  Still has a PR open that she needs Jason to review re ImageMagick perf implications.
    + Cristina grabbed information (e.g., people's public keys) to add to Terraform env.
    + In general, Cristina wants to work with Jason to work on debugging/prognosis performance issues, and she will open a ticket about that.
    + Cristina: would like to discuss how to organize some of these longer-term or tasky issues so they fit well into sprints / epics.
    + Cristina: trade-off between productivity and process.  She got a lot done last week; now she's planning to go backfill issues so we have records of all that productivity.  Dan says sounds great, and don't worry about overdoing the detail when backfilling -- just a note and a pointer is enough.

+ Discussion of individual issues
Overall, this was a very successful sprint, Dan observes.
Dan created Sprint 140 during this meeting; will create them in advance next time.
    + Andrew
        + Did a bunch of stuff tagged for 2.12 release; bringing UI up to feature parity with the UI it's replacing, various housekeeping/cleanup stuff.
        + Plans to switch test runners, uh, something to do with Angular, Karl didn't fully catch the details because dang it folks it's hard to type and listen sometimes, you've got to understand, I'm doing the best I can.  Please.  Please stop looking at me like that.  Is it "Angular" -> "Jest" that's the plan?
            + Karma + Jasmine -> Jest
        + Plans to implement new share modal.
        + Plans to implement global (?) access removal.
            + New access role - "Archive Manager"
        + A few other small things, esp. for upcoming 2.13 release.
    + Jason
        + Mostly working on uploader design (w/ Dan)
        + Priority for this Sprint is https://permanent.atlassian.net/browse/PER-7854 ("Record reprocess task still breaking")
    + Cristina
        + Will throw some issues into Sprint 140
        + Would like to discuss releases and organizing Epics
    + Dan
        + Completed onboarding (closed last couple of issues; thanks Cristina for sending Dan some stuff -- configs? -- that he needed).
        + Plans to take care of 7573 in this new Sprint 140.
        + Lots of time working on architecture and design of new uploader.  Now mostly settled; Dan will follow up in the issue, and execute on the plan, in the new public repository -- issues for this will be in GitHub, not JIRA.

+ Ad hoc discussions:
    + Discussion about working in the open (Cristina)
        + Putting release notes in a public place
            + Jason: Who is the intended audience?  If it's an internal audience, then we should ask whether this is the best way to convey what's happening in releases.  Also, we'll eventually be releasing N times a day, and keeping release notes can be a lot of overhead then.
    + Where to put these system-wide bugs we're finding? (Cristina)
        + Discussion of where to file issues, publicly or privately?  We have purely production service issues -- those should be filed internally.  We have issues that are to do with the closed-source repositories; those get filed in JIRA too, though for different reasons.
            + One lens to view this through: could an external contributor help at all with this bug?
            + Generally we can default to public/open; there is value in seeing closed bugs with "this was a configuration error"
    + Do we have any "quick fix" bugs that newcomers could try?
        + TL;DR: No, not yet.
        + But, hopefully soon we will get to that point.

## Decisions
* Open source repositories will track issues in GitHub; closed repositories will continue to be in BitBucket and JIRA.
* Cristina will pick a spot to put release notes on github.
* We're going to use both JIRA and github for issues, depending on which repo the issue is related.
* We're likely going to transition to a kanban approach (vs sprint planning). (Note that this will not affect the timing or frequency of our scheduled meetings, as we need to do much of the same periodic work.)
* When filing bugs, default to filing publicly unless there's a specific reason to file it privately (e.g., either b/c it's purely a production service issue with no implications for the public project, or because they're bugs in BitBucket-based closed-source repositories).
    * Cristina will use the above principle when dispatching all the tickets she currently needs to find permanent homes for.
* James / Karl / or Dan to convey to Robert that we're moving in this public direction.
