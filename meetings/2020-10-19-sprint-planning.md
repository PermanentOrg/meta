# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-10-19, 1pm CT
Hosted on Google Meet at https://meet.google.com/fsy-jfyd-qei?authuser=0

## Purpose
Engineering team gets in synch on this week's goals and this sprint's status

## Outcomes
Review current status of some active tickets involved in recent work

## Process (Agenda)
Share any good news ya' got!
Sprint Review
Individual Issue Items

--- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

## Roll Call
Add your name, role, location and prefered contact or social info for follow-up – you can select/change your color in the participants dropdown menu at the top right corner.
FIRST POST!  Karl Fogel <kfogel@opentechstrategies.the-usual-domain>
xmunoz
Jason
Andrew
Mithuna
Belated Dan

## Notes


* Good news
    * ughhhhhhhh
    * I went to the Yuba river, and it was lovely🌊
    * Jason: cleaned my apartment! and made my first sourdough!:)
    * I came in to the downtown office and I got Potbelly BLTA for lunch!
    I'm not even normally that big a Potbelly fan, but these days ordering a * sandwich in a sandwich shop counts as high excitement.
    * Put good use to some plants veggies and leaves before winter hits us.. :+!

* Sprint Review
    * Cristina:
        * Will convert design doc into issues.  Taking care of last bits of cleanup that are needed before we begin the migration process.
        * This week:
            * Would like to get infrastructure repository published on GitHub.  Possibly devenv could be rolled into infrastructure, or not, but either way devenv depends on the stuff in infra.
            * There will be a 30m conversation with Cristina + engineering team to go over the new repository / get a review.
            * No more deploying WordPress changes using the normal workflow.  The new workflow will leverage the new infrastructure repository / the new tooling in that repository.


    * Jason:
        * New reprocessing / imagick stuff was pushed!  There was concern that there might be some association with this change and the weekend’s upload errors (but it seems like they aren’t related).
        * Dan says getting new upload flow over the edge first is higher priority than open sourcing mdot in the first half of Q4.

    * Dan:
        * Regarding fixing memory issue in app (Dan’s only JIRA task: 7573): after discussion, we decided to close this ticket as “WONTFIX” because it’s become obsolete in light of other work done recently.  However, we should still, at some point, re-run the tests that alerted us in the first place to the memory issue and see what’s up.
        * Dan will either finish upload service PR #11 by tomorrow afternoon or ask Jason for help.
    * Mithuna:
        * Issue 7611 is almost complete, and was waiting on resolving some unit tests.
    * Andrew:
        * Put a bow on some mdot things: upgrading things in preparation for open-sourcing.
        * Started on Node SDK.
        * Various random infrastructure things took Andrew’s attention this week.

* Discussion of individual issues
    * FamilySearch is broken. Is fixing that a priority?
        * Andrew says: It’s broken because of some changes they (Family search) sprang on us.  This is really a question for the product owner, which is effectively Robert.  Dan will check with Robert to see how to prioritize this.
    * What is the timeline for deploying the upload-service?
        * If the new code is running in the same PHP environment as older code, then there’s a PHP version mismatch to deal with.  Answer: deploy it in its own isolated EC2 micro-instance.  Cristina says that’s fine but make sure to make the appropriate Apache (Or did she say “AWS” not “Apache”?  Karl didn’t catch it for sure; feel free to fix) tweaks.
    * Watching for incoming discussion/review requests from Cristina, who will try not to put anything on anyone’s calendar at the last minute.
