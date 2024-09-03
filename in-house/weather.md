---
icon: cloud-bolt-moon
description: >-
  Check the weather, get information on ongoing severe weather, and check the
  future forecast without leaving your conversation!
---

# Weather

## weather

* Usage: `!weather`

Fetch current and upcoming conditions, search and explore hundreds of weather-focused words, check alert statistics across the country, and fetch information on observation stations and radar installations

### weather alerts

* Usage: `!weather alerts`
* Checks: `server_only`

Shows a statistical summary of active weather alerts

### weather stations

* Usage: `!weather stations`
* Checks: `server_only`

Explore US weather observation stations

### weather stats

* Usage: `!weather stats`

Show statistics about weather feature usage

### weather glossary

* Usage: `!weather glossary [search_term]`
* Checks: `server_only`

Show a glossary, or specify a word to search

### weather now

* Usage: `!weather now [zip_code=None]`

Check current conditions and alerts, specify a zip for conditions at that location

### weather forecast

* Usage: `!weather forecast [zip_code=None]`
* Checks: `server_only`

Fetch your future forecast

### weather profile

* Usage: `!weather profile`

View your weather profile

### weather radars

* Usage: `!weather radars`
* Checks: `server_only`

Explore US weather radar installations

### weather records

* Usage: `!weather records`

Show historical weather records

## weatherset

* Usage: `!weatherset`

Configure settings and features of weather

### weatherset heatalerts

* Usage: `!weatherset heatalerts`
* Cooldown: `1 per 900.0 seconds`

Toggle heat alerts for your saved location

### weatherset freezealerts

* Usage: `!weatherset freezealerts`
* Cooldown: `1 per 900.0 seconds`

Toggle freeze alerts for your saved location

### weatherset zip

* Usage: `!weatherset zip <zip_code>`

Set your zip code for queries

### weatherset severealerts

* Usage: `!weatherset severealerts`
* Cooldown: `1 per 900.0 seconds`

Toggle severe alerts for your saved location
