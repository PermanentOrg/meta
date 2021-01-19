2021-01-14

# Notifications

Attendees: Cecilia, Jason, Mithuna

Goal: single concept of a "notification" with a "call to action."  That's what the API sends the front end and the front end knows how to handle it.

## Initial Notes

- Let's make sure to separate "audit log" from "notification."  Right now the share activity table has both.  (Hence concern about not showing all the activities in the share activity table.)
- The "notification" we send to the front end needn't be backed by one database table
- Proposal about the front end:
    - Send it back a string (the notification) and the necessary link (e.g. view the updated folder).  When the front end navigates to the link, it will ask the backend for the info it needs.
	    - This will not work for many of the CTAs, because they require more information to do a task like approve a request.  It might work for some of them (e.g. "View"), tbd. (See below for details)
    
## Action buttons
- Lots of cross-talk about how to avoid passing VOs back to the front end for the action buttons.  Basically it would involve a lot of other complexity (since all our other endpoints rely on VOs)
- There are some buttons (View, Ignore) that don't require a VO - could just be a link because there's no "Action"
- We have a draft list of buttons associated with each notification.  Possible list of button "types" - to discuss with Bryson next week
- Secondary buttons: after you accept an invitation to an archive, you may get a "View" button (another API response, ofc)

## Notifications by Account, not Archive
- This also requires some settings changes: should be able to manage notification volume by archive
- (note that in-app notifications have no settings options yet, but should)


- Idea from Mithuna: sanitize the outgoing info with "filterClone" (or similar) so that we only pass the front end the pieces of the VO that it needs - e.g. a recordVO might have locationVO, tagVO, etc and we likely don't need to send all that.  (I also like this idea because it prepares us to know exactly which pieces of data are necessary, for a future non-VO-based API.)

## JSON field in the database (in share_activity)
- Jason on json: using the json field in the database robs us of all the power of database validation
- idea: polymorphic table: notifications and share activity linked in one table that includes all common information, links to separate tables with type-specific information

## Notifications table
- Has a "message" field which we don't want to use, so we will construct it from the other fields in that table


## Next steps
- Discussion of database implementation
- Discussion of front end
	- Bryson q: Do we need "ignore" button?  
	- What kinds of action buttons are there?
