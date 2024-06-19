---
description: Warn misbehaving users and take automated actions.
---

# ⚠ Warnings



### Commands[¶](broken-reference)

## warningset

* Usage: `!warningset`
* Restricted to: `GUILD_OWNER`
* Checks: `server_only`

Manage settings for Warnings.

### warningset senddm

* Usage: `!warningset senddm <true_or_false>`
* Checks: `server_only`

Set whether warnings should be sent to users in DMs.

### warningset showmoderator

* Usage: `!warningset showmoderator <true_or_false>`
* Checks: `server_only`

Decide whether the name of the moderator warning a user should be included in the DM to that user.

### warningset warnchannel

* Usage: `!warningset warnchannel [channel=None]`
* Checks: `server_only`

Set the channel where warnings should be sent to.\
\
Leave empty to use the channel !warn command was called in.

### warningset usewarnchannel

* Usage: `!warningset usewarnchannel <true_or_false>`
* Checks: `server_only`

Set if warnings should be sent to a channel set with !warningset warnchannel.

### warningset allowcustomreasons

* Usage: `!warningset allowcustomreasons <allowed>`
* Checks: `server_only`

Enable or disable custom reasons for a warning.

## warnaction

* Usage: `!warnaction`
* Restricted to: `GUILD_OWNER`
* Checks: `server_only`

Manage automated actions for Warnings.\
\
Actions are essentially command macros. Any command can be run\
when the action is initially triggered, and/or when the action\
is lifted.\
Actions must be given a name and a points threshold. When a\
user is warned enough so that their points go over this\
threshold, the action will be executed.

### warnaction delete

* Usage: `!warnaction delete <action_name>`
* Aliases: `del and remove`
* Checks: `server_only`

Delete the action with the specified name.

### warnaction add

* Usage: `!warnaction add <name> <points>`
* Checks: `server_only`

Create an automated action.\
\
Duplicate action names are not allowed.

## warnreason

* Usage: `!warnreason`
* Restricted to: `GUILD_OWNER`
* Checks: `server_only`

Manage warning reasons.\
\
Reasons must be given a name, description and points value. The\
name of the reason must be given when a user is warned.

### warnreason delete

* Usage: `!warnreason delete <reason_name>`
* Aliases: `remove and del`
* Checks: `server_only`

Delete a warning reason.

### warnreason create

* Usage: `!warnreason create <name> <points> <description>`
* Aliases: `add`
* Checks: `server_only`

Create a warning reason.

## reasonlist

* Usage: `!reasonlist`
* Restricted to: `ADMIN`
* Checks: `server_only`

List all configured reasons for Warnings.

## actionlist

* Usage: `!actionlist`
* Restricted to: `ADMIN`
* Checks: `server_only`

List all configured automated actions for Warnings.

## warn

* Usage: `!warn <member> [points=1] <reason>`
* Restricted to: `ADMIN`
* Checks: `server_only`

Warn the user for the specified reason.\
\
number of points the warning should be for. If no number is supplied\
1 point will be given. Pre-set warnings disregard this.\
is reason for the warning. This can be a registered reason,\
or a custom reason if !warningset allowcustomreasons is set.

## warnings

* Usage: `!warnings <member>`
* Restricted to: `ADMIN`
* Checks: `server_only`

List the warnings for the specified user.

## mywarnings

* Usage: `!mywarnings`
* Checks: `server_only`

List warnings for yourself.

## unwarn

* Usage: `!unwarn <member> <warn_id> [reason]`
* Restricted to: `ADMIN`
* Checks: `server_only`

Remove a warning from a user.
