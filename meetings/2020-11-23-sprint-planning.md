# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-11-23, 1pm CT
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
    * Dan
    * xmunoz
    * Jason
    * Mithuna
    * Andrew

## Notes
    * Good News
        * Packing almost done.
        * Lupini beans
        * Dan
            * Health insurance will cover stuff!
            * Mortgage refinancing seems like a good thing but what a waste of time and energy...
            * Reliving childhood in so many ways
                * Latest Example: Animaniacs reboot
                    * It's pretty good! +1
            * I think I have found the recipe for chocolate chip cookies I've always been looking for.
                * https://twitter.com/slifty/status/1330377183739719681/photo/1
        * More sourdough <3
            * NICE! I made my *first* loaf of bread maybe ever ("cornmeal bread")
                * https://twitter.com/slifty/status/1330377183739719681/photo/3

    * Individual issues
        * https://bitbucket.org/permanent-org/website/pull-requests/16
            * I didn't see this commit get merged into staging and prod.
        * A couple of issues have arisen on the new dev environment, which I plan to look at today.
            * https://permanent.atlassian.net/browse/PER-8098
            * https://permanent.atlassian.net/browse/PER-8101
        * Dan
            * What are people's holiday schedules again?
                * Mithuna: Off Tues -> Friday
                * Dan + Andrew: Off Thurs + Friday
                * Jason + Cristina: Available as needed
            * Pairing with Mithuna on PHP
        * Mithuna
            * Need to do a Sentry testing in prod before the new upload is moved to dev, to compare the result.
                * We're *not* going to have old + new upload running side by side, so we would 
                * Note that this is because we don't have feature flags on mdot; in theory the backend could be side by side, it's just that mdot has to pick one or the other.
                * We need to make sure whatever the mobile devs are doing for uploads continues to work +1
        * Andrew
            * Found a bug related to use of unix timestamps instead of datetime strings.

Followup convo:
    mdot open source status?
    Meeting stuff / question.
    Load testing.
     https://github.com/PermanentOrg/infrastructure/pull/12

