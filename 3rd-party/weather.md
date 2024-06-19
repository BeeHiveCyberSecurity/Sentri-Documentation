---
description: >-
  Check the weather, get information on ongoing severe weather, and check the
  future forecast without leaving your conversation!
---

# Weather

## weather (Hybrid Command)

* Usage: `!weather <forecast> <units> <search>`
* Slash Usage: `/weather <forecast> <units> <search>`
* Aliases: `we`

Display weather in a given location\
\
search must take the form of city, state, Country Code\
example: !weather New York, New York, US

### weather coords (Hybrid Command)

* Usage: `!weather coords <forecast> <units> <lat> <lon>`
* Slash Usage: `/weather coords <forecast> <units> <lat> <lon>`
* Aliases: `co and coordinates`

Display weather in a given location\
\
lat and lon specify a precise point on Earth using the\
geographic coordinates specified by latitude (north-south) and longitude (east-west).\
example: !weather coordinates 35 139

### weather zip (Hybrid Command)

* Usage: `!weather zip <forecast> <units> <zipcode>`
* Slash Usage: `/weather zip <forecast> <units> <zipcode>`

Display weather in a given location\
\
zipcode must be a valid ZIP code or ZIP code, Country Code (assumes US otherwise)\
example: !weather zip 20500

### weather set (Hybrid Command)

* Usage: `!weather set`
* Slash Usage: `/weather set`

Set user or server default units

#### weather set server (Hybrid Command)

* Usage: `!weather set server <units>`
* Slash Usage: `/weather set server <units>`
* Restricted to: `MOD`
* Aliases: `server`
* Checks: `server_only`

Sets the server default weather units\
\
units must be one of imperial, metric, or standard (kelvin)

#### weather set user (Hybrid Command)

* Usage: `!weather set user <units>`
* Slash Usage: `/weather set user <units>`

Sets the user default weather units\
\
units must be one of imperial, metric, or standard (kelvin)\
Note: User settings override server settings.

#### weather set bot (Hybrid Command)

* Usage: `!weather set bot <units>`
* Slash Usage: `/weather set bot <units>`
* Restricted to: `MOD`

Sets the bots default weather units\
\
units must be one of imperial, metric, or standard (kelvin)
