---
description: >-
  Modify Discord default objects, like guilds, roles, text channels, voice
  channels, threads and AutoMod!
---

# 🔃 Server Management

## editvoicechannel (Hybrid Command)

* Usage: `!editvoicechannel`
* Slash Usage: `/editvoicechannel`
* Restricted to: `ADMIN`
* Aliases: `editvoiceroom`
* Checks: `server_only`

Commands for edit a voice channel.

### editvoicechannel nsfw (Hybrid Command)

* Usage: `!editvoicechannel nsfw <channel> <nsfw>`
* Slash Usage: `/editvoicechannel nsfw <channel> <nsfw>`
* Checks: `server_only`

Edit voice channel nsfw.

### editvoicechannel position (Hybrid Command)

* Usage: `!editvoicechannel position <channel> <position>`
* Slash Usage: `/editvoicechannel position <channel> <position>`
* Checks: `server_only`

Edit voice channel position.\
\
Warning: Only voice channels are taken into account. Channel 1 is the highest positioned voice channel.\
Channels cannot be moved to a position that takes them out of their current category.

### editvoicechannel userlimit (Hybrid Command)

* Usage: `!editvoicechannel userlimit <channel> <user_limit>`
* Slash Usage: `/editvoicechannel userlimit <channel> <user_limit>`
* Checks: `server_only`

Edit voice channel user limit.\
\
It must be a number between 0 and 99.

### editvoicechannel clone (Hybrid Command)

* Usage: `!editvoicechannel clone <channel> <name>`
* Slash Usage: `/editvoicechannel clone <channel> <name>`
* Checks: `server_only`

Clone a voice channel.

### editvoicechannel name (Hybrid Command)

* Usage: `!editvoicechannel name <channel> <name>`
* Slash Usage: `/editvoicechannel name <channel> <name>`
* Checks: `server_only`

Edit voice channel name.

### editvoicechannel videoqualitymode (Hybrid Command)

* Usage: `!editvoicechannel videoqualitymode <channel> <video_quality_mode>`
* Slash Usage: `/editvoicechannel videoqualitymode <channel> <video_quality_mode>`
* Checks: `server_only`

Edit voice channel video quality mode.\
\
auto = 1\
full = 2

### editvoicechannel delete (Hybrid Command)

* Usage: `!editvoicechannel delete <channel> [confirmation=False]`
* Slash Usage: `/editvoicechannel delete <channel> [confirmation=False]`
* Checks: `server_only`

Delete voice channel.

### editvoicechannel invite (Hybrid Command)

* Usage: `!editvoicechannel invite <channel> [max_age=None] [max_uses=None] [temporary=False] [unique=True]`
* Slash Usage: `/editvoicechannel invite <channel> [max_age=None] [max_uses=None] [temporary=False] [unique=True]`
* Checks: `server_only`

Create an invite for a voice channel.\
\
max\_age: How long the invite should last in days. If it's 0 then the invite doesn't expire.\
max\_uses: How many uses the invite could be used for. If it's 0 then there are unlimited uses.\
temporary: Denotes that the invite grants temporary membership (i.e. they get kicked after they disconnect).\
unique: Indicates if a unique invite URL should be created. Defaults to True. If this is set to False then it will return a previously created invite.

### editvoicechannel permissions (Hybrid Command)

* Usage: `!editvoicechannel permissions <channel> <roles_or_users> <true_or_false> <permissions>`
* Slash Usage: `/editvoicechannel permissions <channel> <roles_or_users> <true_or_false> <permissions>`
* Aliases: `overwrites and perms`
* Checks: `server_only`

Edit voice channel permissions/overwrites.\
\
create\_instant\_invite\
manage\_channels\
add\_reactions\
priority\_speaker\
stream\
read\_messages\
send\_messages\
send\_tts\_messages\
manage\_messages\
embed\_links\
attach\_files\
read\_message\_history\
mention\_everyone\
external\_emojis\
connect\
speak\
mute\_members\
deafen\_members\
move\_members\
use\_voice\_activation\
manage\_roles\
manage\_webhooks\
use\_application\_commands\
request\_to\_speak\
manage\_threads\
create\_public\_threads\
create\_private\_threads\
external\_stickers\
send\_messages\_in\_threads

### editvoicechannel list (Hybrid Command)

* Usage: `!editvoicechannel list`
* Slash Usage: `/editvoicechannel list`
* Checks: `server_only`

List all voice channels in the current server.

### editvoicechannel create (Hybrid Command)

* Usage: `!editvoicechannel create [category=None] <name>`
* Slash Usage: `/editvoicechannel create [category=None] <name>`
* Checks: `server_only`

Create a voice channel.

### editvoicechannel category (Hybrid Command)

* Usage: `!editvoicechannel category <channel> <category>`
* Slash Usage: `/editvoicechannel category <channel> <category>`
* Checks: `server_only`

Edit voice channel category.

### editvoicechannel bitrate (Hybrid Command)

* Usage: `!editvoicechannel bitrate <channel> <bitrate>`
* Slash Usage: `/editvoicechannel bitrate <channel> <bitrate>`
* Checks: `server_only`

Edit voice channel bitrate.\
\
It must be a number between 8000 and\
Level 1: 128000\
Level 2: 256000\
Level 3: 384000

### editvoicechannel syncpermissions (Hybrid Command)

* Usage: `!editvoicechannel syncpermissions <channel> <sync_permissions>`
* Slash Usage: `/editvoicechannel syncpermissions <channel> <sync_permissions>`
* Checks: `server_only`

Edit voice channel sync permissions.

## editthread (Hybrid Command)

* Usage: `!editthread`
* Slash Usage: `/editthread`
* Restricted to: `ADMIN`
* Checks: `server_only`

Commands for edit a text channel.

### editthread pinned (Hybrid Command)

* Usage: `!editthread pinned <thread> <pinned>`
* Slash Usage: `/editthread pinned <thread> <pinned>`
* Checks: `server_only`

Edit thread pinned.

### editthread locked (Hybrid Command)

* Usage: `!editthread locked <thread> <locked>`
* Slash Usage: `/editthread locked <thread> <locked>`
* Checks: `server_only`

Edit thread locked.

### editthread name (Hybrid Command)

* Usage: `!editthread name <thread> <name>`
* Slash Usage: `/editthread name <thread> <name>`
* Checks: `server_only`

Edit thread name.

### editthread create (Hybrid Command)

* Usage: `!editthread create [channel=None] [message=None] <name>`
* Slash Usage: `/editthread create [channel=None] [message=None] <name>`
* Checks: `server_only`

Create a thread.

### editthread list (Hybrid Command)

* Usage: `!editthread list`
* Slash Usage: `/editthread list`
* Checks: `server_only`

List all threads in the current server.

### editthread slowmodedelay (Hybrid Command)

* Usage: `!editthread slowmodedelay <thread> <slowmode_delay>`
* Slash Usage: `/editthread slowmodedelay <thread> <slowmode_delay>`
* Checks: `server_only`

Edit thread slowmode delay.

### editthread archived (Hybrid Command)

* Usage: `!editthread archived <thread> <archived>`
* Slash Usage: `/editthread archived <thread> <archived>`
* Checks: `server_only`

Edit thread archived.

### editthread delete (Hybrid Command)

* Usage: `!editthread delete <thread> [confirmation=False]`
* Slash Usage: `/editthread delete <thread> [confirmation=False]`
* Checks: `server_only`

Delete a thread.

### editthread autoarchiveduration (Hybrid Command)

* Usage: `!editthread autoarchiveduration <thread> <auto_archive_duration>`
* Slash Usage: `/editthread autoarchiveduration <thread> <auto_archive_duration>`
* Checks: `server_only`

Edit thread auto archive duration.

### editthread appliedtags (Hybrid Command)

* Usage: `!editthread appliedtags <thread> <applied_tags>`
* Slash Usage: `/editthread appliedtags <thread> <applied_tags>`
* Checks: `server_only`

Edit thread applied tags.\
\
\
!editthread appliedtags "||\[moderated]"\
!editthread appliedtags "Reporting|⚠️|True" "Bug|🐛"\


### editthread invitable (Hybrid Command)

* Usage: `!editthread invitable <thread> <invitable>`
* Slash Usage: `/editthread invitable <thread> <invitable>`
* Checks: `server_only`

Edit thread invitable.

## edittextchannel (Hybrid Command)

* Usage: `!edittextchannel`
* Slash Usage: `/edittextchannel`
* Restricted to: `ADMIN`
* Checks: `server_only`

Commands for edit a text channel.

### edittextchannel type (Hybrid Command)

* Usage: `!edittextchannel type <channel> <_type>`
* Slash Usage: `/edittextchannel type <channel> <_type>`
* Checks: `server_only`

Edit text channel type.\
\
text: 0\
news: 5\
Currently, only conversion between ChannelType.text and ChannelType.news is supported. This is only available to servers that contain NEWS in Guild.features.

### edittextchannel position (Hybrid Command)

* Usage: `!edittextchannel position <channel> <position>`
* Slash Usage: `/edittextchannel position <channel> <position>`
* Checks: `server_only`

Edit text channel position.\
\
Warning: Only text channels are taken into account. Channel 1 is the highest positioned text channel.\
Channels cannot be moved to a position that takes them out of their current category.

### edittextchannel category (Hybrid Command)

* Usage: `!edittextchannel category <channel> <category>`
* Slash Usage: `/edittextchannel category <channel> <category>`
* Checks: `server_only`

Edit text channel category.

### edittextchannel create (Hybrid Command)

* Usage: `!edittextchannel create [category=None] <name>`
* Slash Usage: `/edittextchannel create [category=None] <name>`
* Checks: `server_only`

Create a text channel.

### edittextchannel permissions (Hybrid Command)

* Usage: `!edittextchannel permissions <channel> <roles_or_users> <true_or_false> <permissions>`
* Slash Usage: `/edittextchannel permissions <channel> <roles_or_users> <true_or_false> <permissions>`
* Aliases: `overwrites and perms`
* Checks: `server_only`

Edit text channel permissions/overwrites.\
\
create\_instant\_invite\
manage\_channels\
add\_reactions\
priority\_speaker\
stream\
read\_messages\
send\_messages\
send\_tts\_messages\
manage\_messages\
embed\_links\
attach\_files\
read\_message\_history\
mention\_everyone\
external\_emojis\
connect\
speak\
mute\_members\
deafen\_members\
move\_members\
use\_voice\_activation\
manage\_roles\
manage\_webhooks\
use\_application\_commands\
request\_to\_speak\
manage\_threads\
create\_public\_threads\
create\_private\_threads\
external\_stickers\
send\_messages\_in\_threads

### edittextchannel syncpermissions (Hybrid Command)

* Usage: `!edittextchannel syncpermissions <channel> <sync_permissions>`
* Slash Usage: `/edittextchannel syncpermissions <channel> <sync_permissions>`
* Checks: `server_only`

Edit text channel syncpermissions with category.

### edittextchannel invite (Hybrid Command)

* Usage: `!edittextchannel invite <channel> [max_age=None] [max_uses=None] [temporary=False] [unique=True]`
* Slash Usage: `/edittextchannel invite <channel> [max_age=None] [max_uses=None] [temporary=False] [unique=True]`
* Checks: `server_only`

Create an invite for a text channel.\
\
max\_age: How long the invite should last in days. If it's 0 then the invite doesn't expire.\
max\_uses: How many uses the invite could be used for. If it's 0 then there are unlimited uses.\
temporary: Denotes that the invite grants temporary membership (i.e. they get kicked after they disconnect).\
unique: Indicates if a unique invite URL should be created. Defaults to True. If this is set to False then it will return a previously created invite.

### edittextchannel clone (Hybrid Command)

* Usage: `!edittextchannel clone <channel> <name>`
* Slash Usage: `/edittextchannel clone <channel> <name>`
* Checks: `server_only`

Clone a text channel.

### edittextchannel nsfw (Hybrid Command)

* Usage: `!edittextchannel nsfw <channel> <nsfw>`
* Slash Usage: `/edittextchannel nsfw <channel> <nsfw>`
* Checks: `server_only`

Edit text channel nsfw.

### edittextchannel name (Hybrid Command)

* Usage: `!edittextchannel name <channel> <name>`
* Slash Usage: `/edittextchannel name <channel> <name>`
* Checks: `server_only`

Edit text channel name.

### edittextchannel topic (Hybrid Command)

* Usage: `!edittextchannel topic <channel> <topic>`
* Slash Usage: `/edittextchannel topic <channel> <topic>`
* Checks: `server_only`

Edit text channel topic.

### edittextchannel defaultautoarchiveduration (Hybrid Command)

* Usage: `!edittextchannel defaultautoarchiveduration <channel> <default_auto_archive_duration>`
* Slash Usage: `/edittextchannel defaultautoarchiveduration <channel> <default_auto_archive_duration>`
* Checks: `server_only`

Edit text channel default auto archive duration.\
\
The new default auto archive duration in minutes for threads created in this channel. Must be one of 60, 1440, 4320, or 10080.

### edittextchannel list (Hybrid Command)

* Usage: `!edittextchannel list`
* Slash Usage: `/edittextchannel list`
* Checks: `server_only`

List all text channels in the current server.

### edittextchannel delete (Hybrid Command)

* Usage: `!edittextchannel delete <channel> [confirmation=False]`
* Slash Usage: `/edittextchannel delete <channel> [confirmation=False]`
* Checks: `server_only`

Delete a text channel.

### edittextchannel slowmodedelay (Hybrid Command)

* Usage: `!edittextchannel slowmodedelay <channel> <slowmode_delay>`
* Slash Usage: `/edittextchannel slowmodedelay <channel> <slowmode_delay>`
* Checks: `server_only`

Edit text channel slowmode delay.\
\
Specifies the slowmode rate limit for user in this channel, in seconds. A value of 0s disables slowmode. The maximum value possible is 21600s.

## editrole (Hybrid Command)

* Usage: `!editrole`
* Slash Usage: `/editrole`
* Restricted to: `ADMIN`
* Checks: `bot_has_server_permissions and server_only`

Commands for edit a role.

### editrole delete (Hybrid Command)

* Usage: `!editrole delete <role> [confirmation=False]`
* Slash Usage: `/editrole delete <role> [confirmation=False]`
* Checks: `bot_has_server_permissions and server_only`

Delete a role.

### editrole name (Hybrid Command)

* Usage: `!editrole name <role> <name>`
* Slash Usage: `/editrole name <role> <name>`
* Checks: `bot_has_server_permissions and server_only`

Edit role name.

### editrole list (Hybrid Command)

* Usage: `!editrole list`
* Slash Usage: `/editrole list`
* Checks: `bot_has_server_permissions and server_only`

List all roles in the current server.

### editrole position (Hybrid Command)

* Usage: `!editrole position <role> <position>`
* Slash Usage: `/editrole position <role> <position>`
* Checks: `bot_has_server_permissions and server_only`

Edit role position.\
\
Warning: The role with a position 1 is the highest role in the Discord hierarchy.

### editrole mentionable (Hybrid Command)

* Usage: `!editrole mentionable <role> <mentionable>`
* Slash Usage: `/editrole mentionable <role> <mentionable>`
* Checks: `bot_has_server_permissions and server_only`

Edit role mentionable.

### editrole color (Hybrid Command)

* Usage: `!editrole color <role> <color>`
* Slash Usage: `/editrole color <role> <color>`
* Aliases: `colour`
* Checks: `bot_has_server_permissions and server_only`

Edit role color.

### editrole permissions (Hybrid Command)

* Usage: `!editrole permissions <role> <permissions>`
* Slash Usage: `/editrole permissions <role> <permissions>`
* Checks: `bot_has_server_permissions and server_only`

Edit role permissions.\
\
Warning: You must use the permissions value in numbers (admnistrator=8).\
You can use: https://discordapi.com/permissions.html

### editrole create (Hybrid Command)

* Usage: `!editrole create [color=None] <name>`
* Slash Usage: `/editrole create [color=None] <name>`
* Checks: `bot_has_server_permissions and server_only`

Create a role.

## editserver (Hybrid Command)

* Usage: `!editserver`
* Slash Usage: `/editserver`
* Restricted to: `ADMIN`
* Checks: `bot_has_server_permissions and server_only`

Commands for edit a server.

### editserver invitesdisabled (Hybrid Command)

* Usage: `!editserver invitesdisabled <invites_disabled>`
* Slash Usage: `/editserver invitesdisabled <invites_disabled>`
* Checks: `bot_has_server_permissions and server_only`

Edit server invites disabled state.

### editserver explicitcontentfilter (Hybrid Command)

* Usage: `!editserver explicitcontentfilter <explicit_content_filter>`
* Slash Usage: `/editserver explicitcontentfilter <explicit_content_filter>`
* Checks: `bot_has_server_permissions and server_only`

Edit server explicit content filter.

### editserver systemchannelflags (Hybrid Command)

* Usage: `!editserver systemchannelflags <system_channel_flags>`
* Slash Usage: `/editserver systemchannelflags <system_channel_flags>`
* Checks: `bot_has_server_permissions and server_only`

Edit server system channel flags.

### editserver afktimeout (Hybrid Command)

* Usage: `!editserver afktimeout <afk_timeout>`
* Slash Usage: `/editserver afktimeout <afk_timeout>`
* Checks: `bot_has_server_permissions and server_only`

Edit server afktimeout.

### editserver community (Hybrid Command)

* Usage: `!editserver community <community>`
* Slash Usage: `/editserver community <community>`
* Checks: `bot_has_server_permissions and server_only`

Edit server community state.

### editserver systemchannel (Hybrid Command)

* Usage: `!editserver systemchannel [system_channel=None]`
* Slash Usage: `/editserver systemchannel [system_channel=None]`
* Checks: `bot_has_server_permissions and server_only`

Edit server system channel.

### editserver verificationlevel (Hybrid Command)

* Usage: `!editserver verificationlevel <verification_level>`
* Slash Usage: `/editserver verificationlevel <verification_level>`
* Checks: `bot_has_server_permissions and server_only`

Edit server verification level.

### editserver premiumprogressbarenabled (Hybrid Command)

* Usage: `!editserver premiumprogressbarenabled <premium_progress_bar_enabled>`
* Slash Usage: `/editserver premiumprogressbarenabled <premium_progress_bar_enabled>`
* Checks: `bot_has_server_permissions and server_only`

Edit server premium progress bar enabled.

### editserver ruleschannel (Hybrid Command)

* Usage: `!editserver ruleschannel [rules_channel=None]`
* Slash Usage: `/editserver ruleschannel [rules_channel=None]`
* Checks: `bot_has_server_permissions and server_only`

Edit server rules channel.

### editserver description (Hybrid Command)

* Usage: `!editserver description [description]`
* Slash Usage: `/editserver description [description]`
* Checks: `bot_has_server_permissions and server_only`

Edit server description.

### editserver name (Hybrid Command)

* Usage: `!editserver name <name>`
* Slash Usage: `/editserver name <name>`
* Checks: `bot_has_server_permissions and server_only`

Edit server name.

### editserver publicupdateschannel (Hybrid Command)

* Usage: `!editserver publicupdateschannel [public_updates_channel=None]`
* Slash Usage: `/editserver publicupdateschannel [public_updates_channel=None]`
* Checks: `bot_has_server_permissions and server_only`

Edit server public updates channel.

### editserver discoverable (Hybrid Command)

* Usage: `!editserver discoverable <discoverable>`
* Slash Usage: `/editserver discoverable <discoverable>`
* Checks: `bot_has_server_permissions and server_only`

Edit server discoverable state.

### editserver preferredlocale (Hybrid Command)

* Usage: `!editserver preferredlocale <preferred_locale>`
* Slash Usage: `/editserver preferredlocale <preferred_locale>`
* Checks: `bot_has_server_permissions and server_only`

Edit server preferred locale.\
\
american\_english = 'en-US'\
british\_english = 'en-GB'\
bulgarian = 'bg'\
chinese = 'zh-CN'\
taiwan\_chinese = 'zh-TW'\
croatian = 'hr'\
czech = 'cs'\
danish = 'da'\
dutch = 'nl'\
finnish = 'fi'\
french = 'fr'\
german = 'de'\
greek = 'el'\
hindi = 'hi'\
hungarian = 'hu'\
italian = 'it'\
japanese = 'ja'\
korean = 'ko'\
lithuanian = 'lt'\
norwegian = 'no'\
polish = 'pl'\
brazil\_portuguese = 'pt-BR'\
romanian = 'ro'\
russian = 'ru'\
spain\_spanish = 'es-ES'\
swedish = 'sv-SE'\
thai = 'th'\
turkish = 'tr'\
ukrainian = 'uk'\
vietnamese = 'vi'

### editserver vanitycode (Hybrid Command)

* Usage: `!editserver vanitycode <vanity_code>`
* Slash Usage: `/editserver vanitycode <vanity_code>`
* Checks: `bot_has_server_permissions and server_only`

Edit server vanity code.

### editserver afkchannel (Hybrid Command)

* Usage: `!editserver afkchannel [afk_channel]`
* Slash Usage: `/editserver afkchannel [afk_channel]`
* Checks: `bot_has_server_permissions and server_only`

Edit server afkchannel.

### editserver defaultnotifications (Hybrid Command)

* Usage: `!editserver defaultnotifications <default_notifications>`
* Slash Usage: `/editserver defaultnotifications <default_notifications>`
* Aliases: `notificationslevel`
* Checks: `bot_has_server_permissions and server_only`

Edit server notification level.

## servermanage

* Usage: `!servermanage`
* Restricted to: `MOD`
* Checks: `server_only`

Manage server icons and banners.

### servermanage icons

* Usage: `!servermanage icons`
* Aliases: `icon`

Manage server icons.

#### servermanage icons list

* Usage: `!servermanage icons list`
* Aliases: `ls`

List the server icons associated with each date.

#### servermanage icons reset

* Usage: `!servermanage icons reset <month> <day>`

Remove a date when to change the server icon.\
\
Parameters\
\----------\
month: int\
The month to remove any server icon changes, expressed as a number.\
day: int\
The day of the month to remove any server icon changes, expressed as a number.

#### servermanage icons show

* Usage: `!servermanage icons show <iconName>`

Show a server icon from the database.\
\
Parameters\
\----------\
iconName: str\
The icon name you wish to show.

#### servermanage icons remove

* Usage: `!servermanage icons remove <iconName>`
* Aliases: `del, delete, and rm`

Remove a server icon from the database.\
\
Parameters\
\----------\
iconName: str\
The icon name you wish to remove.

#### servermanage icons set

* Usage: `!servermanage icons set <month> <day> <iconName>`

Set when to change the server icon.\
\
Parameters\
\----------\
month: int\
The month to change the server icon, expressed as a number.\
day: int\
The day of the month to change the server icon, expressed as a number.\
iconName: str\
The name of the server icon to change to. The icon should already be added.

#### servermanage icons add

* Usage: `!servermanage icons add <iconName>`
* Aliases: `create`

Add a server icon to the database.\
\
Parameters\
\----------\
iconName: str\
The name of the icon you wish to add.\
image: attachment\
The server icon, included as an attachment.

### servermanage banners

* Usage: `!servermanage banners`
* Aliases: `banner`

Manage server banners.

#### servermanage banners remove

* Usage: `!servermanage banners remove <bannerName>`
* Aliases: `del, delete, and rm`

Remove a server banner from the database.\
\
Parameters\
\----------\
bannerName: str\
The banner name you wish to remove.

#### servermanage banners set

* Usage: `!servermanage banners set <month> <day> <bannerName>`

Set when to change the server banner.\
\
Parameters\
\----------\
month: int\
The month to change the server banner, expressed as a number.\
day: int\
The day of the month to change the server banner, expressed as a number.\
bannerName: str\
The name of the server banner to change to. The banner should already be added.

#### servermanage banners list

* Usage: `!servermanage banners list`
* Aliases: `ls`

List the server banners associated with each date.

#### servermanage banners reset

* Usage: `!servermanage banners reset <month> <day>`

Remove a date when to change the server banner.\
\
Parameters\
\----------\
month: int\
The month to remove any server banner changes, expressed as a number.\
day: int\
The day of the month to remove any server banner changes, expressed as a number.

#### servermanage banners show

* Usage: `!servermanage banners show <bannerName>`

Show a server banner from the database.\
\
Parameters\
\----------\
bannerName: str\
The banner name you wish to show.

#### servermanage banners add

* Usage: `!servermanage banners add <bannerName>`
* Aliases: `create`

Add a server banner to the database.\
\
Parameters\
\----------\
bannerName: str\
The name of the banner you wish to add.\
image: attachment\
The server banner, included as an attachment.
