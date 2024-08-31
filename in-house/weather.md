---
icon: cloud-bolt-moon
description: >-
  Check the weather, get information on ongoing severe weather, and check the
  future forecast without leaving your conversation!
---

# Weather

## weatherset

* Usage: `!weatherset`

Set your weather preferences

### weatherset stats

* Usage: `!weatherset stats`

Show statistics about weather feature usage

### weatherset zip

* Usage: `!weatherset zip <zip_code>`

Save your zip code to the bot's config

### weatherset severealerts

* Usage: `!weatherset severealerts <enable>`

Enable or disable weather alerts for your saved zip code

## weather

* Usage: `!weather`

Interact with the weather.gov API to fetch weather data via Discord

### weather alerts

* Usage: `!weather alerts`
* Checks: `server_only`

Shows a statistical summary of active weather alerts

### weather now

* Usage: `!weather now`

Fetch your current conditions and now-cast

### weather radars

* Usage: `!weather radars`
* Checks: `server_only`

Fetch and display radar stations information.

### weather forecast

* Usage: `!weather forecast`
* Checks: `server_only`

Fetch your future forecast

### weather stations

* Usage: `!weather stations`
* Checks: `server_only`

Fetch and display weather observation stations.

### weather glossary

* Usage: `!weather glossary [search_term]`
* Checks: `server_only`

Show a glossary, or specify a word to search
