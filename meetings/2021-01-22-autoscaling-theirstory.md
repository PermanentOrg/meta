# TheirStory getting errors back from the SDK

## Purpose
Have a plan for how TheirStory users can import to Permanent without the current set of errors.

## Outcomes
- Short-term plan to mitigate CPU overuse theirstory (with estimate of when it will be up)
- Longer-term plan to mitigate CPU overuse theirstory(probably autoscaling)
If these can be the same then great!
– generic risk assessment and strategy for CPU overuse

## Process

- Andrew: Quick explanation of what's going on/the problem
- Cecilia: Current status of autoscaling
- All: brainstorm ideas to prevent this immediately (space out imports even more? change S3 settings to reduce CPU usage?)
- Cecilia and Andrew: Estimate time to get autoscaling back

## Roll call
- Cecilia
- Andrew
- Robert

## Notes

What's going on?
- there's nothing unique about what TheirStory is doing, just that they have  a lot of large files.  Regular users could trigger it with large files, too.  e.g. 5 big videos + 45 photos
- When there are enough files on our server in progress of uploading then incoming files are likely to time out
- currently: files to webserver, then go to S3
- new process: files to S3, then back to us for processing, then back to S3 in a different location

State of Autoscaling
- previously, our provisioner platform had troubles dealing with auto-scaling groups and targeting them for code deployment
- Since the new infra rollout, these issues have been resolved and the using auto-scaling groups in our configuration is now possible

Short-term
- Rate-limiting: TheirStory could relatively easily add a queueing system, per Dennis.
  - This is a worse outcome, but it's possible
  - Most APIs do have rate limits, Robert points out
  - Will most TheirStory users have a big backlog like OJMCHE?
  - Heavy usage from direct Permanent.org users wouldn't be reflected in their queue
  - (We expected "make a video, export a video" not pull in a ton of videos at once)
- The other thing we could do in the short term is use a bigger box (double it) (costs money)
- We could hardcode two (or more) boxes into the setup (instead of autoscaling) (also money)
- Have TheirStory indicate to backlog users to go slow, without an engineering solution
- Dedicated machine for TheirStory
	- Sits idle when not in use by TS, only benefit to TS is that the load from Permanent users doesn't affect this box
- Rate limit in the SDK (of the queue-based solutions this is my favorite)
  - Would be more engineering
  - This would be a fine experience for TheirStory because their UI doesn't expect a quick response
  - May be eventually needed at large scale regardless
