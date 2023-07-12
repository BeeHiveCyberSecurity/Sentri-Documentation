---
description: Configure Defender and modify it's settings with the following commands.
---

# 🤖 Commands

## dset

* Usage: `!dset`
* Restricted to: `ADMIN`
* Aliases: `defset`
* Checks: `server_only`

Defender system settings

### dset commentanalysis

* Usage: `!dset commentanalysis`
* Restricted to: `ADMIN`
* Aliases: `ca`

Comment analysis configuration\
\
See [Chat Monitoring](introduction/chat-monitoring.md) for more information about this module

#### dset commentanalysis reason

* Usage: `!dset commentanalysis reason <reason>`

Sets a reason for the action (modlog use)

#### dset commentanalysis deletemessage

* Usage: `!dset commentanalysis deletemessage <on_or_off>`

Toggles whether to delete the offending message

#### dset commentanalysis threshold

* Usage: `!dset commentanalysis threshold <threshold>`

Sets the threshold that will trigger CA's action (20-100)

#### dset commentanalysis wdchecks

* Usage: `!dset commentanalysis wdchecks [conditions]`

Implement advanced Warden based checks\
\
Issuing this command with no arguments will show the current checks\
Passing 'remove' will remove existing checks

#### dset commentanalysis enable

* Usage: `!dset commentanalysis enable <on_or_off>`

Toggles comment analysis

#### dset commentanalysis rank

* Usage: `!dset commentanalysis rank <rank>`

Sets target rank

#### dset commentanalysis token

* Usage: `!dset commentanalysis token <token>`

Sets Perspective API token\
\
https://developers.perspectiveapi.com/s/docs

#### dset commentanalysis action

* Usage: `!dset commentanalysis action <action>`

Sets action (ban, kick, softban, punish or none (notification only))

#### dset commentanalysis wipe

* Usage: `!dset commentanalysis wipe <days>`

Sets how many days worth of messages to delete if the action is ban\
\
Setting 0 will not delete any message

#### dset commentanalysis attributes

* Usage: `!dset commentanalysis attributes`

Setup the attributes that CA will check

### dset invitefilter

* Usage: `!dset invitefilter`
* Restricted to: `ADMIN`
* Aliases: `if`

Invite filter auto module configuration\
\
See !defender status for more information about this module

#### dset invitefilter rank

* Usage: `!dset invitefilter rank <rank>`

Sets target rank

#### dset invitefilter action

* Usage: `!dset invitefilter action <action>`

Sets action (ban, kick, softban, punish or none (deletion only))

#### dset invitefilter excludeowninvites

* Usage: `!dset invitefilter excludeowninvites <yes_or_no>`

Excludes this server's invites from the filter

#### dset invitefilter wdchecks

* Usage: `!dset invitefilter wdchecks [conditions]`

Implement advanced Warden based checks\
\
Issuing this command with no arguments will show the current checks\
Passing 'remove' will remove existing checks

#### dset invitefilter deletemessage

* Usage: `!dset invitefilter deletemessage <on_or_off>`

Toggles whether to delete the invite's message

#### dset invitefilter enable

* Usage: `!dset invitefilter enable <on_or_off>`

Toggle invite filter

### dset importfrom

* Usage: `!dset importfrom <server>`

Import the configuration from another server\
\
This is permitted only if the command issuer is admin in both servers

### dset rank3

* Usage: `!dset rank3`
* Restricted to: `ADMIN`

Rank 3 configuration\
\
See !defender status for more information about this rank

#### dset rank3 joineddays

* Usage: `!dset rank3 joineddays <days>`

Days since join required to be considered Rank 3

#### dset rank3 minmessages

* Usage: `!dset rank3 minmessages <messages>`

Minimum messages required to reach Rank 3

### dset general

* Usage: `!dset general`
* Restricted to: `ADMIN`

Defender general settings

#### dset general trustedroles

* Usage: `!dset general trustedroles <roles>`

Sets the trusted roles\
\
Users belonging to this role will be classified as Rank 1

#### dset general reset

* Usage: `!dset general reset [confirmation=False]`

Resets Defender configuration for this server

#### dset general punishrole

* Usage: `!dset general punishrole <role>`

Sets the role that will be assigned to misbehaving users\
\
Note: this will only be assigned if the 'action' of a module\
is set to 'punish'.

#### dset general helperroles

* Usage: `!dset general helperroles <roles>`

Sets the helper roles\
\
See !defender status for more information about these roles

#### dset general countmessages

* Usage: `!dset general countmessages <on_or_off>`

Toggles message count (and rank 4)

#### dset general enable

* Usage: `!dset general enable <on_or_off>`

Toggle defender system

#### dset general notifychannel

* Usage: `!dset general notifychannel <channel>`

Sets the channel where notifications will be sent\
\
This channel should preferably be staff readable only as it could\
potentially contain sensitive info

#### dset general punishmessage

* Usage: `!dset general punishmessage <message>`

Sets the messages that I will send after assigning the punish role\
\
Supports context variables. You can add the following to your message:\
$user -> User's name + tag\
$user\_name -> User's name\
$user\_display -> User's nickname if set or user's name\
$user\_id -> User's id\
$user\_mention -> User's mention\
$user\_nickname -> User's nickname if set or 'None'

#### dset general notifyrole

* Usage: `!dset general notifyrole <role>`

Sets the role that will be pinged in case of alerts

### dset raiderdetection

* Usage: `!dset raiderdetection`
* Restricted to: `ADMIN`
* Aliases: `rd`

Raider detection auto module configuration\
\
See !defender status for more information about this module

#### dset raiderdetection messages

* Usage: `!dset raiderdetection messages <messages>`

Sets messages (User posted X messages in Y minutes)

#### dset raiderdetection rank

* Usage: `!dset raiderdetection rank <rank>`

Sets target rank

#### dset raiderdetection wipe

* Usage: `!dset raiderdetection wipe <days>`

Sets how many days worth of messages to delete if the action is ban\
\
Setting 0 will not delete any message

#### dset raiderdetection enable

* Usage: `!dset raiderdetection enable <on_or_off>`

Toggles raider detection

#### dset raiderdetection action

* Usage: `!dset raiderdetection action <action>`

Sets action (ban, kick, softban, punish or none (notify only))

#### dset raiderdetection wdchecks

* Usage: `!dset raiderdetection wdchecks [conditions]`

Implement advanced Warden based checks\
\
Issuing this command with no arguments will show the current checks\
Passing 'remove' will remove existing checks

#### dset raiderdetection minutes

* Usage: `!dset raiderdetection minutes <minutes>`

Sets minutes (User posted X messages in Y minutes)

### dset warden

* Usage: `!dset warden`
* Restricted to: `ADMIN`
* Aliases: `wd`

Warden auto module configuration\
\
See !defender status for more information about this module

#### dset warden enable

* Usage: `!dset warden enable <on_or_off>`

Toggles warden

### dset vaporize

* Usage: `!dset vaporize`
* Restricted to: `ADMIN`

Vaporize manual module configuration\
\
See !defender status for more information about this module

#### dset vaporize enable

* Usage: `!dset vaporize enable <on_or_off>`

Toggle vaporize manual module

#### dset vaporize maxtargets

* Usage: `!dset vaporize maxtargets <max_targets>`

Sets the maximum amount of targets (1-999)\
\
By default only a maximum of 15 users can be vaporized at once

### dset alert

* Usage: `!dset alert`
* Restricted to: `ADMIN`

Alert manual module configuration\
\
See !defender status for more information about this module

#### dset alert enable

* Usage: `!dset alert enable <on_or_off>`

Toggle alert manual module

### dset joinmonitor

* Usage: `!dset joinmonitor`
* Restricted to: `ADMIN`
* Aliases: `jm`

Join monitor auto module configuration\
\
See !defender status for more information about this module

#### dset joinmonitor minutes

* Usage: `!dset joinmonitor minutes <minutes>`

Sets minutes (X users joined in Y minutes)

#### dset joinmonitor users

* Usage: `!dset joinmonitor users <users>`

Sets users (X users joined in Y minutes)

#### dset joinmonitor notifynew

* Usage: `!dset joinmonitor notifynew <hours>`

Enables notifications for users younger than X hours\
\
Use 0 hours to disable notifications

#### dset joinmonitor wdchecks

* Usage: `!dset joinmonitor wdchecks [conditions]`

Implement advanced Warden based checks\
\
Issuing this command with no arguments will show the current checks\
Passing 'remove' will remove existing checks

#### dset joinmonitor enable

* Usage: `!dset joinmonitor enable <on_or_off>`

Toggles join monitor

#### dset joinmonitor verificationlevel

* Usage: `!dset joinmonitor verificationlevel`

Raises the server's verification level on raids\
\
You can find a full description of Discord's verification levels in\
the server's settings "Moderation" tab.\
\
Verification levels:\
0 - No action\
1 - Low: verified email\
2 - Medium: must be registered for longer than 5 minutes\
3 - High: must be a member of this server for longer than 10 minutes\
4 - Highest: must have a verified phone on their Discord account

### dset voteout

* Usage: `!dset voteout`
* Restricted to: `ADMIN`

Voteout manual module configuration\
\
See !defender status for more information about this module

#### dset voteout action

* Usage: `!dset voteout action <action>`

Sets action (ban, kick, softban, punish)

#### dset voteout votes

* Usage: `!dset voteout votes <votes>`

Sets required votes number for it to pass

#### dset voteout enable

* Usage: `!dset voteout enable <on_or_off>`

Toggles voteout

#### dset voteout wipe

* Usage: `!dset voteout wipe <days>`

Sets how many days worth of messages to delete if the action is ban\
\
Setting 0 will not delete any message

#### dset voteout rank

* Usage: `!dset voteout rank <rank>`

Sets target rank

### dset silence

* Usage: `!dset silence`
* Restricted to: `ADMIN`

Silence manual module configuration\
\
See !defender status for more information about this module

#### dset silence enable

* Usage: `!dset silence enable <on_or_off>`

Toggle silence manual module

### dset emergency

* Usage: `!dset emergency`
* Restricted to: `ADMIN`

Emergency mode configuration\
\
See !defender status for more information about emergency mode

#### dset emergency minutes

* Usage: `!dset emergency minutes <minutes>`

Sets max inactivity minutes for staff\
\
After X minutes of inactivity following an alert emergency\
mode will be engaged and helper roles will be able to use\
the emergency modules.

#### dset emergency modules

* Usage: `!dset emergency modules`

Sets emergency modules\
\
Emergency modules will be rendered available to helper roles\
during emergency mode. Selecting no modules to this command will\
disable emergency mode.\
Available emergency modules: voteout, vaporize, silence

## defender

* Usage: `!defender`
* Restricted to: `MOD`
* Aliases: `def`
* Checks: `server_only`

Defender commands reserved to staff

### defender messages

* Usage: `!defender messages`
* Aliases: `msg`

Access recorded messages of users / channels

#### defender messages user

* Usage: `!defender messages user <user>`

Shows recent messages of a user

#### defender messages channel

* Usage: `!defender messages channel <channel>`

Shows recent messages of a channel

#### defender messages exportuser

* Usage: `!defender messages exportuser <user>`

Exports recent messages of a user to a file

#### defender messages exportchannel

* Usage: `!defender messages exportchannel <channel>`

Exports recent messages of a channel to a file

### defender emergency

* Usage: `!defender emergency <on_or_off>`

Manually engage or turn off emergency mode\
\
Upon activation, staff will be pinged and any module\
that is set to be active in emergency mode will be rendered\
available to helpers

### defender freshmeat

* Usage: `!defender freshmeat [hours=24] [keywords]`

Returns a list of the new users of the day\
\
Can be filtered. Supports wildcards (\* and ?)

### defender updates

* Usage: `!defender updates`

Shows all the past announcements of Defender

### defender notifynew

* Usage: `!defender notifynew <hours>`

Sends you a DM if a user younger than X hours joins\
\
Use 0 hours to disable notifications

### defender status

* Usage: `!defender status`

Shows overall status of the Defender system

### defender memberranks

* Usage: `!defender memberranks`

Counts how many members are in each rank

### defender warden

* Usage: `!defender warden`
* Restricted to: `ADMIN`
* Aliases: `wd`

Warden rules management\
\
See !defender status for more information about Warden

#### defender warden export

* Usage: `!defender warden export <name>`

Sends the rule as a YAML file

#### defender warden list

* Usage: `!defender warden list`

Lists existing rules

#### defender warden debug

* Usage: `!defender warden debug <_id> <event> [rank=None]`

Simulate and give a detailed summary of an event\
\
A Warden event must be passed with the proper target ID (user or local message)\
\
When this command is issued all the rules registered to the event will be\
processed in a safe way against the target, if any.\
If the target satisfies the conditions, _only_ the heatpoint related actions\
will be carried on.\
The heatpoint actions will be "sandboxed", so the newly added heatpoints won't\
have any effect outside this test.\
Remember that Warden evaluates each condition in order and stops at the first failed\
root condition: the last condition that is listed in a failed rule is where Warden\
stopped evaluating them.\
If a valid Rank is also passed it will be used in place of the target's real\
rank during the test.\
See the documentation for a full list of Warden events.\
\
Example:\
!def warden debug \<valid\_user\_id> on-user-join\
!def warden debug \<valid\_message\_id> on-message\
!def warden debug \<valid\_message\_id> on-message-edit 3

#### defender warden exportall

* Usage: `!defender warden exportall`

Sends all the rules as a tar.gz archive

#### defender warden add

* Usage: `!defender warden add <rule>`

Adds a new rule

#### defender warden show

* Usage: `!defender warden show <name>`

Shows a rule

#### defender warden run

* Usage: `!defender warden run <name>`

Runs a rule against the whole userbase\
\
Confirmation is asked before execution.

#### defender warden remove

* Usage: `!defender warden remove <name>`

Removes a rule by name

#### defender warden find

* Usage: `!defender warden find <text>`
* Aliases: `search`

Search for text in existing rules

#### defender warden upload

* Usage: `!defender warden upload`
* Cooldown: `1 per 86400.0 seconds`

Starts a rule upload session

#### defender warden memory

* Usage: `!defender warden memory [keywords]`

Shows or resets the memory of Warden\
\
Can be filtered. Supports wildcards (\* and ?)

#### defender warden removeall

* Usage: `!defender warden removeall`

Removes all rules

### defender monitor

* Usage: `!defender monitor [keywords]`

Shows recent events that might require your attention\
\
Can be filtered. Supports wildcards (\* and ?)

### defender identify

* Usage: `!defender identify <user>`

Shows a member's rank + info

## alert

* Usage: `!alert`
* Aliases: `staff`
* Cooldown: `1 per 120.0 seconds`
* Checks: `server_only`

Alert the staff members

## vaporize

* Usage: `!vaporize <members>`
* Checks: `server_only`

Gets rid of bad actors in a quick and silent way\
\
Works only on Rank 3 and under

## voteout

* Usage: `!voteout <user>`
* Cooldown: `1 per 22.0 seconds`
* Checks: `server_only`

Initiates a vote to expel a user from the server\
\
Can be used by members with helper roles during emergency mode

## silence

* Usage: `!silence <rank>`
* Checks: `server_only`

Enables server wide message autodeletion for the specified rank (and below)\
\
Passing 0 will disable this.
