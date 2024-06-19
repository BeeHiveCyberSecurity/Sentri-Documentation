---
description: Get alerts about, and check the status of, streamers on various sites!
---

# Streams

## twitchstream

* Usage: `!twitchstream <channel_name>`
* Checks: `server_only`

Check if a Twitch channel is live.

## youtubestream

* Usage: `!youtubestream <channel_id_or_name>`
* Cooldown: `1 per 30.0 seconds`
* Checks: `server_only`

Check if a YouTube channel is live.

## picarto

* Usage: `!picarto <channel_name>`
* Checks: `server_only`

Check if a Picarto channel is live.

## streamalert

* Usage: `!streamalert`
* Restricted to: `MOD`
* Checks: `server_only`

Manage automated stream alerts.

### streamalert twitch

* Usage: `!streamalert twitch <channel_name> [discord_channel=operator.attrgetter('channel')]`

Manage Twitch stream notifications.

#### streamalert twitch channel

* Usage: `!streamalert twitch channel <channel_name> [discord_channel=operator.attrgetter('channel')]`

Toggle alerts in this or the given channel for a Twitch stream.

### streamalert picarto

* Usage: `!streamalert picarto <channel_name> [discord_channel=operator.attrgetter('channel')]`

Toggle alerts in this channel for a Picarto stream.

### streamalert stop

* Usage: `!streamalert stop [_all=False]`

Disable all stream alerts in this channel or server.\
\
!streamalert stop will disable this channel's stream\
alerts.\
\
Do !streamalert stop yes to disable all stream alerts in\
this server.

### streamalert list

* Usage: `!streamalert list`

List all active stream alerts in this server.

### streamalert youtube

* Usage: `!streamalert youtube <channel_name_or_id> [discord_channel=operator.attrgetter('channel')]`

Toggle alerts in this channel for a YouTube stream.

## streamset

* Usage: `!streamset`
* Restricted to: `MOD`

Manage stream alert settings.

### streamset message

* Usage: `!streamset message`
* Checks: `server_only`

Manage custom messages for stream alerts.

#### streamset message mention

* Usage: `!streamset message mention <message>`
* Checks: `server_only`

Set stream alert message when mentions are enabled.\
\
Use {mention} in the message to insert the selected mentions.\
Use {stream} in the message to insert the channel or username.\
Use {stream.display\_name} in the message to insert the channel's display name (on Twitch, this may be different from {stream}).\
\
For example: !streamset message mention {mention}, {stream.display\_name} is live!

#### streamset message nomention

* Usage: `!streamset message nomention <message>`
* Checks: `server_only`

Set stream alert message when mentions are disabled.\
\
Use {stream} in the message to insert the channel or username.\
Use {stream.display\_name} in the message to insert the channel's display name (on Twitch, this may be different from {stream}).\
\
For example: !streamset message nomention {stream.display\_name} is live!

#### streamset message clear

* Usage: `!streamset message clear`
* Checks: `server_only`

Reset the stream alert messages in this server.

### streamset autodelete

* Usage: `!streamset autodelete <on_off>`
* Checks: `server_only`

Toggle alert deletion for when streams go offline.

### streamset mention

* Usage: `!streamset mention`
* Checks: `server_only`

Manage mention settings for stream alerts.

#### streamset mention online

* Usage: `!streamset mention online`
* Aliases: `here`
* Checks: `server_only`

Toggle the @​here mention.

#### streamset mention role

* Usage: `!streamset mention role <role>`
* Checks: `server_only`

Toggle a role mention.

#### streamset mention all

* Usage: `!streamset mention all`
* Aliases: `everyone`
* Checks: `server_only`

Toggle the @​everyone mention.

### streamset usebuttons

* Usage: `!streamset usebuttons`
* Checks: `server_only`

Toggle whether to use buttons for stream alerts.

### streamset ignorereruns

* Usage: `!streamset ignorereruns`
* Checks: `server_only`

Toggle excluding rerun streams from alerts.

### streamset ignoreschedule

* Usage: `!streamset ignoreschedule`
* Checks: `server_only`

Toggle excluding YouTube streams schedules from alerts.\
\
golivealert

* Usage: `!golivealert [channel=None]`
* Restricted to: `MOD`
* Checks: `server_only`

Set the channel for live alerts.

## discordstreamsset

* Usage: `!discordstreamsset`
* Restricted to: `MOD`
* Checks: `server_only`

Change settings for the live alerts from the server's own VC's.

### discordstreamsset ignored

* Usage: `!discordstreamsset ignored`

List ignored voice channels.

### discordstreamsset ignore

* Usage: `!discordstreamsset ignore <channel>`

Ignore a voice channel.
