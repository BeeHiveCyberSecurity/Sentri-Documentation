---
description: >-
  Allocate a Discord voice channel to show the time in specific timezones.
  Updates every hour.
---

# ⌛ Time Channels

## timezones

* Usage: `!timezones`
* Checks: `server_only`

See the time in all the configured timezones for this server.

## timechannelset

* Usage: `!timechannelset`
* Restricted to: `ADMIN`
* Aliases: `tcset`

Manage channels which will show the time for a timezone.

### timechannelset short

* Usage: `!timechannelset short <timezone>`

Get the short identifier for the main create command.\
\
The list of acceptable timezones is here (the "TZ database name" column):\
https://en.wikipedia.org/wiki/List\_of\_tz\_database\_time\_zones#List\
\
There is a fuzzy search, so you shouldn't need to enter the region.\
\
Please look at `!help tcset create` for more information.\
\
**Examples:**\
\- `!tcset short New York`\
\- `!tcset short UTC`\
\- `!tcset short London`\
\- `!tcset short Europe/London`

### timechannelset remove

* Usage: `!timechannelset remove <channel>`

Delete and stop updating a channel.\
\
For the argument, you can use its ID or mention (type #!channelname)\
\
**Example:**\
\- `!tcset remove #!channelname` (the ! is how to mention voice channels)\
\- `!tcset remove 834146070094282843`

### timechannelset create

* Usage: `!timechannelset create <string>`

Set up a time channel in this server.

{% hint style="warning" %}
If you move the channel into a category

**click 'Keep Current Permissions'**&#x20;

**in the sync permissions dialogue.**
{% endhint %}

**How to use this command:**\
\
First, use the `!tcset short <long_tz>` to get the short identifier for the timezone of your choice.\
\
Once you've got a short identifier from tcset short, you can use it in this command.\
Simply put curly brackets, { and } around it, and it will be replaced with the time.\
\
**For example**, running !tcset short new york gives a short identifier of fv.\
This can then be used like so:\
`!tcset create 🕑️ New York: {fv}`.\
\
You could also use two in one, for example\
`!tcset create UK: {ni} FR: {nr}`\
\
The default is 12 hour time, but you can use {shortid-24h} for 24 hour time,\
eg `{ni-24h}`\
\
**More Examples:**\
\- `!tcset create 🕑️ New York: {fv}`\
\- `!tcset create 🌐 UTC: {qw}`\
\- `!tcset create {ni-24h} in London`\
\- `!tcset create US Pacific: {qv-24h}`
