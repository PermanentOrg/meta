# PERMANENT LEGACY FOUNDATION – Permanent.org
Sprint Planning
2020-11-02, 1pm CT
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
  * Dan Schultz
  * Mithuna 
  * xmunoz
  * Andrew
  * Jason

## Notes
  * Good News
    * I saw my friends on Halloween, and we performed a ritual and then played a musical procession around my block🎶
    * Andrew: ate a lot of M&M's and had some good cookout food in my friend's backyard
    * Nearly 2m Oregonian ballots have been counted, as of 9am Pacific
    * Dan: Trick or treating with the kids worked out (though was super inefficient) -- we drove around to family nearby and knocked on their doors!
    * Mithuna:: My daughter enjoyed trick-o-treat and brought home lot of candies.. not sure what to do with it..
  * Sprint Review
    * We need to do a better job of note taking!  Could folks write their own notes in here before we fully log off?
    * Dan
      * Upload service PR is merged, I'm integrating it into vagrant / dev / infrastructure now.
      * This sprint I'll be pairing with Jason and Mithuna to finish the upload integration with mdot and php.
    * Mithuna : 
      * Weekly upload reports are back.
      * Will be working on API endpoint for new upload-service
      * Also the metadata overhaul
    * Cristina
        * ImageMagick Incantations, then a functional test:
        * https://github.com/PermanentOrg/functional-test
    * Andrew
      * Done
        * New access role (manager)
        * Prep for publish on node-sdk
      * Will do
        * Prep for m-dot open source!


  * Individual issues
    * Functional tests
    * Reprocessing files
      * Try running these broken files on the new environment just to find out if those don't fail with upgraded deps
      * Timeouts aren't being enforced on long-running/hung conversions, perhaps the check that stops unneeded re-processes isn't ever getting hit
        * Look at moving the "have we failed too many times?" check from the end of the process, after a failure, to the beginning
    * Uploader service- will it have Sentry integration? Answer: yes
      * https://github.com/PermanentOrg/upload-service/issues/3
    * Thoughts on port forwarding for vagrant? (should I expose the uploader service or keep the footprint light?)
