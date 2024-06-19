---
description: Stat channels for your server.
---

# Info Channels

Create a channel with updating server info\


{% hint style="info" %}
This relies on editing channels, which is a strictly rate-limited activity. As such, updates will not be frequent. Currently capped at 1 per 5 minutes per server. No, we won't change them for you.
{% endhint %}

## infochannel

* Usage: `!infochannel`
* Restricted to: `ADMIN`

Toggle info channel for this server

## infochannelset

* Usage: `!infochannelset`
* Restricted to: `ADMIN`
* Aliases: `icset`

Toggle different types of infochannels

### infochannelset togglechannel

* Usage: `!infochannelset togglechannel <channel_type> [enabled=None]`

Toggles the infochannel for the specified channel type.\
\
Valid Types are:\
\- members: Total members on the server\
\- humans: Total members that aren't bots\
\- boosters: Total amount of boosters\
\- bots: Total bots\
\- roles: Total number of roles\
\- channels: Total number of channels excluding infochannels,\
\- online: Total online members,\
\- offline: Total offline members,

### infochannelset togglerole

* Usage: `!infochannelset togglerole <role> [enabled=None]`

Toggle an infochannel that shows the count of users with the specified role

### infochannelset name

* Usage: `!infochannelset name <channel_type> [text]`

Change the name of the infochannel for the specified channel type.\
\
{count} must be used to display number of total members in the server.\
Leave blank to set back to default.\
\
Examples:\
\- !infochannelset name members Cool Cats: {count}\
\- !infochannelset name bots {count} Robot Overlords\
\
Valid Types are:\
\- members: Total members on the server\
\- humans: Total members that aren't bots\
\- boosters: Total amount of boosters\
\- bots: Total bots\
\- roles: Total number of roles\
\- channels: Total number of channels excluding infochannels\
\- online: Total online members\
\- offline: Total offline members\
\
Warning: This command counts against the channel update rate limit and may be queued.

### infochannelset rolename

* Usage: `!infochannelset rolename <role> [text]`

Change the name of the infochannel for specific roles.\
\
{count} must be used to display number members with the given role.\
{role} can be used for the roles name.\
Leave blank to set back to default.\
\
Default is set to: {role}: {count}\
\
Examples:\
\- !infochannelset rolename @Patrons {role}: {count}\
\- !infochannelset rolename Elite {count} members with {role} role\
\- !infochannelset rolename "Space Role" Total boosters: {count}\
\
Warning: This command counts against the channel update rate limit and may be queued.
