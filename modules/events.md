---
description: Host and manage events in your server with a variety of customization options
---

# 📅 Events

Create an event, set a channel for submissions and entry requirements/options.\
Users can enter the event and make submissions according to the parameters set.

## enotify

* Usage: `!enotify`
* Checks: `server_only`

Enable/Disable event notifications for yourself\
\
You will be notified when events start and end

## enter

* Usage: `!enter`
* Checks: `server_only`

Enter an event if one exists

## events

* Usage: `!events`
* Checks: `server_only`

Create, manage and view events

### events staffrole

* Usage: `!events staffrole <role>`

Add/Remove staff roles\
\
If ping staff is enabled, these roles will be pinged on event completion

### events delete

* Usage: `!events delete`

Delete an event outright

### events resultdelete

* Usage: `!events resultdelete`

(Toggle) Include event results in the messages to delete on cleanup\
\
If this is on when an event is deleted and the user chooses to clean up the messages,\
the results announcement will also be deleted

### events pingstaff

* Usage: `!events pingstaff`

(Toggle) Ping staff on event completion

### events emoji

* Usage: `!events emoji <emoji>`

Set the default emoji for votes\
\
Changing the vote emoji only affects events created after this is changed.\
Existing events will still use the previous emoji for votes

### events create

* Usage: `!events create`

Create a new event

### events notifyrole

* Usage: `!events notifyrole <role>`

Add/Remove notify roles\
\
These roles will be pinged on event start and completion

### events view

* Usage: `!events view`

View the current events and settings

### events blacklistrole

* Usage: `!events blacklistrole <role>`

Add/Remove blacklisted roles\
\
These roles are not allowed to enter events, but can still vote on them

### events blacklistuser

* Usage: `!events blacklistuser <user>`

Add/Remove blacklisted users\
\
These users are not allowed to enter events, but can still vote on them

### events extend

* Usage: `!events extend <time_string>`

Extend the runtime of an event\
\
**Examples**\
10d - 10 days\
7d4h - 7 days 4 hours

### events end

* Usage: `!events end`

End an event early, counting votes/announcing the winner\
\
This will also delete the event afterwards

### events remove

* Usage: `!events remove <user>`

Remove a user from an active event

### events autodelete

* Usage: `!events autodelete`

(Toggle) Auto delete events from config when they complete\
\
If auto delete is enabled, the messages in the event channel will need to be cleaned up manually

### events shorten

* Usage: `!events shorten <time_string>`

Shorten the runtime of an event\
\
**Examples**\
10d - 10 days\
7d4h - 7 days 4 hours
