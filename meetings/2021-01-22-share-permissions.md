Roll Call
Mithuna
Cecilia, Jason, Andrew

Purpose
	* Get a better understanding of how permissions work across archives.

Outcomes
	* Create a matrix type document describing the power of each role
	* Understand and document what each role can do. 

Process

2 levels of access permission
- Member level
	- Permission granted to accounts to the entire contents of a specific archive
- Share level
	- Permission granted to accounts with access to a specific archive on a specific item 
	
	
Currently, web-app *grants* access by share level and *removes* access by member level

Examples:
    Archive A shares item X with Archive B with Owner share permissions
    - Account 1 is owner of Archive A
    - Account 2 is owner of Archive B
    - Account 3 is viewer of Archive A
    - Account 3 is curator of Archive B
    
    - Account 1 -> Archive A -> item X: All owner permissions
    - Account 2 -> Archive B -> item X: All owner permissions
    - Account 3 -> Archive A -> item X: Viewer permissions
    - Account 3 -> Archive B -> item X: Curator permissions
    
    
"Manager" is only available as a member level, but all others have the same meanings/access whether they are used as a member level or a share level.

Mithuna (account) has the Flower Archive (as owner) with the Narcissus item.
Cecilia (account) has the Skiing Archive (as owner).
Cecilia (account) is not a member of the Flower Archive.
The Flower Archive shares the Narcissus item with the Skiing Archive (as owner)

Cecilia (account) has owner access to Narcissus (when checked into the Skiing Archive)


Is each access level a strict superset of the next lower level? Yes!
This may not always be the case, would need to keep in mind


https://permanent.atlassian.net/wiki/spaces/EN/pages/1187938307/Permissions
https://docs.google.com/spreadsheets/d/1yT8Q8lpkCZrnQ6a13DXxxJQU5H-ffbp081qP33CnVdg/edit#gid=0

Action definitions:
Create
- Uploading a file
- Creating a new folder
	
Read
- Navigating into a folder
- Reading metadata for a specific folder
- Reading metadata for a specific file
- Downloading

Edit
- Changing metadata on an existing folder
- Changing metadata on an existing file

Delete
- Deleting contents of an existing folder
	- may or may not apply to the 'root' folder of a share
- Deleting an existing files

Upload
- Is an existing permission, but is a duplicate of Create(?)
- Need to check if new upload checks these separately

Publish
- Adding files to public folder
- Adding folders to public folder

Move
- Move an existing file
- Move an existing folder
- Only within the topmost folder that access is granted on; cannot move across that boundary (but can copy & delete, given appropriate permissions)

Share (share level permissions) 
- Add archives to a shared item
- Change archive access on a shared item
- Remove archive access to a shared item

Archive Share (member level permissions)
- Add members to an archive
- Change member access to an archive
- Remove member access to an archive

Link
- Deprecated
- This previous capability is why we have both folder ID and folder_linkID

Ownership (only relevant as a "member level" permission, not "share level")
- Can transfer archive ownership to another account

To determine the actions available to an account checked into a given archive on a specific item, use the lesser permissions granted between "member level" and "share level" (phrasing can be cleaned up)


Questions:
    - Does delete permission allow deleting a folder, or only for children of the folder? The web-app does not surface that ability; unsure if restricted by the backend
    - Is the Ownership permission actually used?
    
Later work:
	- Remove the Upload permission; it is checked differently by different upload endpoints, and every permission level that has Upload also has Create
    Old upload service was checking for create permision when allowing to upload.
    Post ->create and upload
    postMetaBatch -> create
    RegisterRecord -> create
	- Remove Link permission; remove folder_linkID
	- Bring back user facing list of permissions for access levels
	
Thoughts:
    UI hints if a user has more permissive access in another archive than they currently have? "You could do this in ____ archive if you want just not here" type deal
