---
description: >-
  Don't forget anything anymore! Reminders in DMs, channels, FIFO commands
  scheduler, say scheduler... With 'Me Too', snooze and buttons.
---

# ⏰ Reminders

## remindme (Hybrid Command)

* Usage: `!remindme <time> [message_or_text]`
* Slash Usage: `/remindme <time> [message_or_text]`

Create a reminder with optional reminder text or message.\
\
The specified time can be fuzzy parsed or use the kwargs in, on and every to find a repeat rule and your text.\
You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.\
Use !reminder timetips to display tips for time parsing.\
\
**Examples:**\
\- !remindme in 8min45sec to do that thing\
\- !remindme to water my plants in 2 hours\
\- !remindme in 3 days\
\- !remindme 8h\
\- !remindme every 1 week to take out the trash\
\- !remindme in 1 hour \<message\_link>\
\- !remindme at 10h to add some feature to my codes

## remind (Hybrid Command)

* Usage: `!remind <destination> <targets> <time> [message_or_text]`
* Slash Usage: `/remind <destination> <targets> <time> [message_or_text]`
* Checks: `server_only`

Create a reminder with optional reminder text or message, in a channel with an user/role ping.\
\
The specified time can be fuzzy parsed or use the kwargs in, on and every to find a repeat rule and your text.\
You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.\
Use !reminder timetips to display tips for time parsing.\
\
Examples:\
\- !remind #destination @user1 @user2 @user2 in 2 hours to buy a gift

## reminder (Hybrid Command)

* Usage: `!reminder`
* Slash Usage: `/reminder`
* Aliases: `reminders`

List, edit and delete existing reminders, or create FIFO/commands or Say reminders.

### reminder say (Hybrid Command)

* Usage: `!reminder say <destination> <time> <text>`
* Slash Usage: `/reminder say <destination> <time> <text>`
* Restricted to: `GUILD_OWNER`
* Checks: `server_only`

Create a reminder who will say/send text.\
\
The specified time can be fuzzy parsed or use the kwargs in, on and every to find a repeat rule and your text.\
You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.\
Use !reminder timetips to display tips for time parsing.\
\
Examples:\
\- !reminder say #destination "at 9h every day" Hello everyone!

### reminder timetips (Hybrid Command)

* Usage: `!reminder timetips`
* Slash Usage: `/reminder timetips`
* Aliases: `parsingtips`

Show time parsing tips.

### reminder expires (Hybrid Command)

* Usage: `!reminder expires <reminder> <time>`
* Slash Usage: `/reminder expires <reminder> <time>`
* Aliases: `expiresat`

Edit the expires time of an existing Reminder from its ID.\
\
\- Use last to edit your last created reminder.\
\- Use next to edit your next triggered reminder.\
It's the same converter as for creation, but without the option of repetition.

### reminder text (Hybrid Command)

* Usage: `!reminder text <reminder> <text>`
* Slash Usage: `/reminder text <reminder> <text>`

Edit the text of an existing Reminder from its ID.\
\
\- Use last to edit your last created reminder.\
\- Use next to edit your next triggered reminder.

### reminder fifo (Hybrid Command)

* Usage: `!reminder fifo <destination> <time> <command>`
* Slash Usage: `/reminder fifo <destination> <time> <command>`
* Restricted to: `ADMIN`
* Aliases: `command`
* Checks: `server_only`

Create a FIFO/command reminder. The chosen command will be executed with you as invoker. Don't provide the prefix.\
\
The specified time can be fuzzy parsed or use the kwargs in, on and every to find a repeat rule and your text.\
You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.\
Use !reminder timetips to display tips for time parsing.\
\
Examples:\
\- !reminder fifo #destination "at 10h every day" ping

### reminder remove (Hybrid Command)

* Usage: `!reminder remove <reminders>`
* Slash Usage: `/reminder remove <reminders>`
* Aliases: `delete and -`

Remove existing Reminder(s) from their IDs.\
\
\- Use last to remove your last created reminder.\
\- Use next to remove your next triggered reminder.

### reminder edit (Hybrid Command)

* Usage: `!reminder edit <reminder>`
* Slash Usage: `/reminder edit <reminder>`

Edit an existing Reminder from its ID.\
\
\- Use last to edit your last created reminder.\
\- Use next to edit your next triggered reminder.

### reminder repeat (Hybrid Command)

* Usage: `!reminder repeat <reminder> <repeat>`
* Slash Usage: `/reminder repeat <reminder> <repeat>`

Edit the repeat of an existing Reminder from its ID.\
\
\- Use last to edit your last created reminder.\
\- Use next to edit your next triggered reminder.\
\
Allowed **intervals** are:\
• years/year/y\
• months/month/mo\
• weeks/week/w\
• days/day/d\
• hours/hour/hrs/hr/h\
• minutes/minute/mins/min/m\
\
You can combine **relative intervals** like this:\
• 1y 1mo 2 days -5h

### reminder clear (Hybrid Command)

* Usage: `!reminder clear [confirmation=False]`
* Slash Usage: `/reminder clear [confirmation=False]`

Clear all your existing reminders.

### reminder list (Hybrid Command)

* Usage: `!reminder list [card=False] [content_type=None] [sort=expire]`
* Slash Usage: `/reminder list [card=False] [content_type=None] [sort=expire]`

List your existing reminders.\
\
Sort options:\
\- expire: Display them in order of next triggering.\
\- created: Display them in order of creating.\
\- id: Display them in order of their ID.

### reminder timezone (Hybrid Command)

* Usage: `!reminder timezone <timezone>`
* Slash Usage: `/reminder timezone <timezone>`

Set your timezone for the time converter.\
\
Europe/Paris, America/New\_York...
