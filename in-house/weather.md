---
description: >-
  Check the weather, get information on ongoing severe weather, and check the
  future forecast without leaving your conversation!
icon: cloud-bolt-moon
---

# Weather

## weatherset

* Usage: `!weatherset`

Set your weather preferences

### weatherset stats

* Usage: `!weatherset stats`

Show statistics about zip code subscriptions and alert subscriptions

### weatherset zip

* Usage: `!weatherset zip <zip_code>`

Save your zip code to the bot's config

> #### zip\_code: str
>
> ```
> A single word, if not using slash and multiple words are necessary use a quote e.g "Hello world".
> ```

### weatherset alerts

* Usage: `!weatherset alerts <enable>`

Enable or disable weather alerts for your saved zip code

> #### enable: bool
>
> ```
> Can be 1, 0, true, false, t, f
> ```

## weather

* Usage: `!weather`

Interact with the weather.gov API to fetch weather data via Discord

### weather now

* Usage: `!weather now`

Fetch your current conditions and now-cast

### weather forecast

* Usage: `!weather forecast`
* Checks: `server_only`

Fetch your future forecast

### weather alerts

* Usage: `!weather alerts`
* Checks: `server_only`

Shows a statistical summary of active weather alerts

### weather radars

* Usage: `!weather radars`
* Checks: `server_only`

Fetch and display radar stations information.

### weather glossary

* Usage: `!weather glossary [search_term]`
* Checks: `server_only`

Show a glossary, or specify a word to search

> #### search\_term: str = None
>
> ```
> A single word, if not using slash and multiple words are necessary use a quote e.g "Hello world".
> ```

### weather stations

* Usage: `!weather stations`
* Checks: `server_only`

Fetch and display weather observation stations.
