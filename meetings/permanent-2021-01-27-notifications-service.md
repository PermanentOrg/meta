# Notifications Service

Purpose: Agree as a team on the implementation plan for the new notifications service

Proposal: Build a new microservice in Typescript, similar to the upload-service.

## Goals for the new service:
    
1. Open source the new service (in a usable way for other people)
2. Morale boost for the team, because it feels more "finished" as a standalone service
3. Fresh codebase with correct process(es), preparing for a better-designed future
4. Avoid Permanent-specific logic and requirements so that it can be reused more easily (this might be too difficult and we'll have to balance it with engineering time/velocity)

## Consequences of microservice architecture

1. Separate database (so limited data integrity checking at db level)

## Details, Details

Should notifications be updated when the underlying data is updated? Example: invite at one permission level, then invite at a lower permission level. Maybe the easier thing (of not updating the data) is actually the right thing.

Eventually we want to move the emails out into this notifications service, too.
As well as SMS and potentially push notifications

Client will unify old notifications and new ones (coming from the new service)

Database of the future: MariaDB or Postgres?  (No strong opinion from Mithuna and Andrew on this)

## Deployment plan

Add another box to run this service?  Possibly one instance to run all the microservices, actually.  We think this is a good time!

TypeScript! It would be helpful to have Andrew share his dev setup. What are the alternatives? We could do Laravel in PHP; 

Still to-do: research existing solutions to potentially drop in and/or extend to suit our needs

Timeline: get an initial "hello world" demo by Feb 5

## Authn/authz

Do the API gateway/wrapper first?  So that we don't have to use PHP for the authn/authz piece?

Main concern is that we need to do this incrementally - can we?  How much time is the right amount of time to devote to it?

## Concerns
Rich text, eg archive names; how do we get data back from this microservice? What about actions? Still need to think about this! In theory we could include {URL, method, arguments} and have the client do the rest...?

Eventually this will also include push notifications, SMS, ah see above :)

Notifications don't interact with the SDK or integrations.

What happens to old data?
	- migration strategy depending on notification type
	- for at least some notification types, probably we do need to migrate data
		- how many current notifications are unread?
			(status new) ~= (status seen + status read)
			~72k notifications altogether
		- we are *Permanent*; probably we should not delete things
