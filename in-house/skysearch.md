---
description: Interact with the sky by getting information on aircraft and airports easily.
---

# SkySearch

## aircraft

* Usage: `!aircraft`
* Aliases: `skysearch`
* Checks: `server_only`

Summon the aircraft panel

### aircraft pia

* Usage: `!aircraft pia`
* Checks: `server_only`

View live aircraft using private ICAO addresses

### aircraft ladd

* Usage: `!aircraft ladd`
* Checks: `server_only`

Get information on LADD-restricted aircraft

### aircraft radius

* Usage: `!aircraft radius <lat> <lon> <radius>`
* Checks: `server_only`

Get information about aircraft within a specified radius.

### aircraft alertchannel

* Usage: `!aircraft alertchannel [channel=None]`
* Checks: `server_only`

Set or clear a channel to send emergency squawk alerts to. Clear with no channel.

### aircraft scroll

* Usage: `!aircraft scroll`
* Checks: `server_only`

Scroll through available planes.

### aircraft showalertchannel

* Usage: `!aircraft showalertchannel`
* Checks: `server_only`

Show alert task status and output if set

### aircraft military

* Usage: `!aircraft military`
* Checks: `server_only`

Get information about military aircraft.

### aircraft icao

* Usage: `!aircraft icao <hex_id>`
* Checks: `server_only`

Get information about an aircraft by its 24-bit ICAO Address

### aircraft export

* Usage: `!aircraft export <search_type> <search_value> <file_format>`
* Checks: `server_only`

Search aircraft by ICAO, callsign, squawk, or type and export the results.

### aircraft stats

* Usage: `!aircraft stats`
* Checks: `server_only`

Get statistics about SkySearch and the data used here

### aircraft type

* Usage: `!aircraft type <aircraft_type>`
* Checks: `server_only`

Get information about aircraft by its type.

### aircraft alertrole

* Usage: `!aircraft alertrole [role=None]`
* Checks: `server_only`

Set or clear a role to mention when new emergency squawks occur. Clear with no role.

### aircraft autoicao

* Usage: `!aircraft autoicao [state=None]`
* Checks: `server_only`

Enable or disable automatic ICAO lookup.

### aircraft squawk

* Usage: `!aircraft squawk <squawk_value>`
* Checks: `server_only`

Get information about an aircraft by its squawk code.

### aircraft reg

* Usage: `!aircraft reg <registration>`
* Checks: `server_only`

Get information about an aircraft by its registration.

### aircraft callsign

* Usage: `!aircraft callsign <callsign>`
* Checks: `server_only`

Get information about an aircraft by its callsign.

## airport

* Usage: `!airport`
* Aliases: `groundsearch`
* Checks: `server_only`

Summon SkySearch ground search panel

### airport forecast

* Usage: `!airport forecast <code>`
* Checks: `server_only`

Get the future weather format for an airport by ICAO or IATA code.

### airport navaid

* Usage: `!airport navaid <code>`
* Checks: `server_only`

Query navaid information by ICAO code.

### airport info

* Usage: `!airport info [code=None]`
* Checks: `server_only`

Query airport information by ICAO or IATA code.

### airport runway

* Usage: `!airport runway <code>`
* Checks: `server_only`

Query runway information by ICAO code.
