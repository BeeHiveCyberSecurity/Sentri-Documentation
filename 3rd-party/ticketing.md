---
description: >-
  Support ticket system with multi-panel functionality. Simple, pretty, works
  well, saves logs for staff.
---

# 🎫 Ticketing

## add (Hybrid Command)

* Usage: `!add <user>`
* Slash Usage: `/add <user>`
* Checks: `server_only`

Add a user to your ticket

## renameticket (Hybrid Command)

* Usage: `!renameticket <new_name>`
* Slash Usage: `/renameticket <new_name>`
* Checks: `server_only`

Rename your ticket channel

## close (Hybrid Command)

* Usage: `!close [reason]`
* Slash Usage: `/close [reason]`
* Checks: `server_only`

Close your ticket\
\
**Examples**\
!close - closes ticket with no reason attached\
!close thanks for helping! - closes with reason "thanks for helping!"\
!close 1h - closes in 1 hour with no reason attached\
!close 1m thanks for helping! - closes in 1 minute with reason "thanks for helping!"

## tickets

* Usage: `!tickets`
* Restricted to: `ADMIN`
* Aliases: `tset`
* Checks: `server_only`

Base support ticket settings

### tickets ticketname

* Usage: `!tickets ticketname <panel_name> <ticket_name>`

Set the default ticket channel name for a panel\
\
You can include the following in the name\
{num} - Ticket number\
{user} - user's name\
{displayname} - user's display name\
{id} - user's ID\
{shortdate} - mm-dd\
{longdate} - mm-dd-yyyy\
{time} - hh-mm AM/PM according to bot host system time\
\
You can set this to {default} to use default "Ticket-Username

### tickets embed

* Usage: `!tickets embed <color> <channel> <title> <description>`

Create an embed for ticket panel buttons to be added to

### tickets row

* Usage: `!tickets row <panel_name> <row>`

Set the row of a panel's button (0 - 4)

### tickets addmodal

* Usage: `!tickets addmodal <panel_name> <field_name>`

Add a modal field a ticket panel\
\
Ticket panels can have up to 5 fields per modal for the user to fill out before opening a ticket.\
If modal fields are added and have required fields,\
the user will have to fill them out before they can open a ticket.\
\
There is no toggle for modals, if a panel has them it will use them, if they don't then it just opens the ticket\
When the ticket is opened, it sends the modal field responses in an embed below the ticket message\
\
**Note**\
field\_name is just the name of the field stored in config,\
it won't be shown in the modal and should not have spaces in it\
\
\
Specify an existing field name to delete a modal field (non-case-sensitive)

### tickets maxclaims

* Usage: `!tickets maxclaims <panel_name> <amount>`

Set how many staff members can claim/join a ticket before the join button is disabled (If using threads)

### tickets selfclose

* Usage: `!tickets selfclose`

(Toggle) If users can close their own tickets

### tickets interactivetranscript

* Usage: `!tickets interactivetranscript`
* Aliases: `intertrans, itrans, and itranscript`

(Toggle) Interactive transcripts\
\
Transcripts will be an interactive html file to visualize the conversation from your browser.

### tickets buttontext

* Usage: `!tickets buttontext <panel_name> <button_text>`

Set the button text for a support ticket panel

### tickets view

* Usage: `!tickets view`

View support ticket settings

### tickets cleanup

* Usage: `!tickets cleanup`

Cleanup tickets that no longer exist

### tickets usethreads

* Usage: `!tickets usethreads <panel_name>`

Toggle whether a certain panel uses threads or channels

### tickets blacklist

* Usage: `!tickets blacklist <user_or_role>`

Add/Remove users or roles from the blacklist\
\
Users and roles in the blacklist will not be able to create a ticket

### tickets updatemessage

* Usage: `!tickets updatemessage <source> <target>`

Update a message with another message (Target gets updated using the source)

### tickets addpanel

* Usage: `!tickets addpanel <panel_name>`

Add a support ticket panel

### tickets buttoncolor

* Usage: `!tickets buttoncolor <panel_name> <button_color>`

Set the button color for a support ticket panel

### tickets viewmodal

* Usage: `!tickets viewmodal <panel_name>`

View/Delete a ticket message for a support ticket panel

### tickets selfmanage

* Usage: `!tickets selfmanage`

(Toggle) If users can manage their own tickets\
\
Users will be able to add/remove others to their support ticket

### tickets openrole

* Usage: `!tickets openrole <panel_name> <role>`

Add/Remove roles required to open a ticket for a specific panel\
\
Specify the same role to remove it

### tickets closemodal

* Usage: `!tickets closemodal <panel_name>`

Throw a modal when the close button is clicked to enter a reason

### tickets category

* Usage: `!tickets category <panel_name> <category>`

Set the category ID for a ticket panel

### tickets maxtickets

* Usage: `!tickets maxtickets <amount>`

Set the max tickets a user can have open at one time of any kind

### tickets dm

* Usage: `!tickets dm`

(Toggle) The bot sending DM's for ticket alerts

### tickets noresponse

* Usage: `!tickets noresponse <hours>`

Auto-close ticket if opener doesn't say anything after X hours of opening\
\
Set to 0 to disable this\
\
If using thread tickets, this translates to the thread's "Hide after inactivity" setting.\
Your options are:\
\- 1 hour\
\- 24 hours (1 day)\
\- 72 hours (3 days)\
\- 168 hours (1 week)\
Tickets will default to the closest value you select.

### tickets buttonemoji

* Usage: `!tickets buttonemoji <panel_name> <emoji>`

Set the button emoji for a support ticket panel

### tickets addmessage

* Usage: `!tickets addmessage <panel_name>`

Add a message embed to be sent when a ticket is opened\
\
You can include any of these in the embed to be replaced by their value when the message is sent\
{username} - Person's Discord username\
{mention} - This will mention the user\
{id} - This is the ID of the user that created the ticket\
\
The bot will walk you through a few steps to set up the embed

### tickets autoadd

* Usage: `!tickets autoadd`

(Toggle) Auto-add support and panel roles to thread tickets\
\
Adding a user to a thread pings them, so this is off by default

### tickets altchannel

* Usage: `!tickets altchannel <panel_name> <channel>`

Set an alternate channel that tickets will be opened under for a panel\
\
If the panel uses threads, this needs to be a normal text channel.\
If the panel uses channels, this needs to be a category.\
\
If the panel is a channel type and a channel is used, the bot will use the category associated with the channel.\
\
To remove the alt channel, specify the existing one

### tickets channel

* Usage: `!tickets channel <panel_name> <channel>`

Set the channel ID where a ticket panel is located

### tickets logchannel

* Usage: `!tickets logchannel <panel_name> <channel>`

Set the logging channel for each panel's tickets

### tickets supportrole

* Usage: `!tickets supportrole <role> [mention=False]`

Add/Remove ticket support roles (one at a time)\
\
**Optional**: include true for mention to have that role mentioned when a ticket is opened\
\
To remove a role, simply run this command with it again to remove it

### tickets threadclose

* Usage: `!tickets threadclose`

(Toggle) Thread tickets being closed & archived instead of deleted

### tickets setuphelp

* Usage: `!tickets setuphelp`

Ticket Setup Guide

### tickets overview

* Usage: `!tickets overview [channel]`

Set a channel for the live overview message\
\
The overview message shows all active tickets across all configured panels for a server.

### tickets toggle

* Usage: `!tickets toggle <panel_name>`

Toggle a panel on/off\
\
Disabled panels will still show the button but it will be disabled

### tickets viewmessages

* Usage: `!tickets viewmessages <panel_name>`

View/Delete a ticket message for a support ticket panel

### tickets transcript

* Usage: `!tickets transcript`

(Toggle) Ticket transcripts\
\
Closed tickets will have their transcripts uploaded to the log channel

### tickets priority

* Usage: `!tickets priority <panel_name> <priority>`

Set the priority order of a panel's button

### tickets panelrole

* Usage: `!tickets panelrole <panel_name> <role> [mention=False]`

Add/Remove roles for a specific panel\
\
To remove a role, simply run this command with it again to remove it\
\
**Optional**: include true for mention to have that role mentioned when a ticket is opened\
\
These roles are a specialized subset of the main support roles.\
Use this role type if you want to isolate specific groups to a certain panel.

### tickets panelmessage

* Usage: `!tickets panelmessage <panel_name> <message>`

Set the message ID of a ticket panel\
Run this command in the same channel as the ticket panel message

### tickets modaltitle

* Usage: `!tickets modaltitle <panel_name> [title]`

Set a title for a ticket panel's modal

### tickets selfrename

* Usage: `!tickets selfrename`

(Toggle) If users can rename their own tickets

### tickets overviewmention

* Usage: `!tickets overviewmention`

Toggle whether channels are mentioned in the active ticket overview

### tickets panels

* Usage: `!tickets panels`

View/Delete currently configured support ticket panels
