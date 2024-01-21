---
description: View embeds showcasing the supplied color and information about it
---

# 🍪 Colors

## color

* Usage: `!color`
* Aliases: `colour`

Group command for color commands

### color rgb

* Usage: `!color rgb <highest> <r> <g> <b>`

Provides the hexadecimal value and HSL value of the rgb value given. Each value must have a space between them. Highest argument must be 1 or 255, indicating the highest value of a single value (r, g, or b).

### color hex

* Usage: `!color hex <hexa>`

Provides the RGB value and HSL value of a passed hexadecimal value. Hexadecimal value must in the format of something like #ffffff or 0xffffff to be used.

### color name

* Usage: `!color name <name>`

Provides the hexadecimal value, RGB value and HSL value of a passed color. For example, pass red or blue as the name argument.

### color decimal

* Usage: `!color decimal <decimal>`

Provides the RGB value of the decimal value given.

### color msgshort

* Usage: `!color msgshort <enable>`
* Restricted to: `ADMIN`

Enable or disable the in-message shortcut.\
\
In-message shortcuts can be used by using the hex, rgb or name after a # in the middle of a message, as follows:\
\
\#000000 (hex)\
\#1,1,1 (rgb)\
\#black (named)

### color hsl

* Usage: `!color hsl <h> <s> <l>`

Provides the hexadecimal value and the RGB value of the hsl value given. Each value must have a space between them.
