---
description: Distribute a server-specific, make-believe currency
---

# 💰 Economy

## bank

* Usage: `!bank`
* Checks: `server_only_check`

Base command to manage the bank.

### bank set

* Usage: `!bank set <to> <creds>`
* Restricted to: `ADMIN`
* Checks: `is_owner_if_bank_global`

Set the balance of a user's bank account.\
\
Putting + or - signs before the amount will add/remove currency on the user's bank account instead.\
\
Examples:\
\- !bank set @Twentysix 26 - Sets balance to 26\
\- !bank set @Twentysix +2 - Increases balance by 2\
\- !bank set @Twentysix -6 - Decreases balance by 6\
\
**Arguments**\
\
\- The user to set the currency of.\
\- The amount of currency to set their balance to.

### bank balance

* Usage: `!bank balance [user=operator.attrgetter('author')]`

Show the user's account balance.\
\
Example:\
\- !bank balance\
\- !bank balance @Twentysix\
\
**Arguments**\
\
\- The user to check the balance of. If omitted, defaults to your own balance.

### bank transfer

* Usage: `!bank transfer <to> <amount>`

Transfer currency to other users.\
\
This will come out of your balance, so make sure you have enough.\
\
Example:\
\- !bank transfer @Twentysix 500\
\
**Arguments**\
\
\- The user to give currency to.\
\- The amount of currency to give.

## payday

* Usage: `!payday`
* Checks: `server_only_check`

Get some free currency.\
\
The amount awarded and frequency can be configured.

## leaderboard

* Usage: `!leaderboard [top=10] [show_global=False]`
* Checks: `server_only_check`

Print the leaderboard.\
\
Defaults to top 10.\
\
Examples:\
\- !leaderboard\
\- !leaderboard 50 - Shows the top 50 instead of top 10.\
\- !leaderboard 100 yes - Shows the top 100 from all servers.\
\
**Arguments**\
\
\- How many positions on the leaderboard to show. Defaults to 10 if omitted.\
\- \<show\_global> Whether to include results from all servers. This will default to false unless specified.

## payouts

* Usage: `!payouts`
* Checks: `server_only_check`

Show the payouts for the slot machine.

## slot

* Usage: `!slot <bid>`
* Checks: `server_only_check`

Use the slot machine.\
\
Example:\
\- !slot 50\
\
**Arguments**\
\
\- The amount to bet on the slot machine. Winning payouts are higher when you bet more.

## economyset

* Usage: `!economyset`
* Restricted to: `ADMIN`
* Checks: `is_owner_if_bank_global and server_only_check`

Base command to manage Economy settings.

### economyset slotmin

* Usage: `!economyset slotmin <bid>`

Set the minimum slot machine bid.\
\
Example:\
\- !economyset slotmin 10\
\
**Arguments**\
\
\- The new minimum bid for using the slot machine. Default is 5.

### economyset rolepaydayamount

* Usage: `!economyset rolepaydayamount <role> <creds>`

Set the amount earned each payday for a role.\
\
Set to 0 to remove the payday amount you set for that role.\
\
Only available when not using a global bank.\
\
Example:\
\- !economyset rolepaydayamount @Members 400\
\
**Arguments**\
\
\- The role to assign a custom payday amount to.\
\- The new amount to give when using the payday command.

### economyset paydayamount

* Usage: `!economyset paydayamount <creds>`

Set the amount earned each payday.\
\
Example:\
\- !economyset paydayamount 400\
\
**Arguments**\
\
\- The new amount to give when using the payday command. Default is 120.

### economyset paydaytime

* Usage: `!economyset paydaytime <duration>`

Set the cooldown for the payday command.\
\
Examples:\
\- !economyset paydaytime 86400\
\- !economyset paydaytime 1d\
\
**Arguments**\
\
\- The new duration to wait in between uses of payday. Default is 5 minutes.\
Accepts: seconds, minutes, hours, days, weeks (if no unit is specified, the duration is assumed to be given in seconds)

### economyset slotmax

* Usage: `!economyset slotmax <bid>`

Set the maximum slot machine bid.\
\
Example:\
\- !economyset slotmax 50\
\
**Arguments**\
\
\- The new maximum bid for using the slot machine. Default is 100.

### economyset slottime

* Usage: `!economyset slottime <duration>`

Set the cooldown for the slot machine.\
\
Examples:\
\- !economyset slottime 10\
\- !economyset slottime 10m\
\
**Arguments**\
\
\- The new duration to wait in between uses of the slot machine. Default is 5 seconds.\
Accepts: seconds, minutes, hours, days, weeks (if no unit is specified, the duration is assumed to be given in seconds)

### economyset showsettings

* Usage: `!economyset showsettings`

Shows the current economy settings
