---
description: Basic encode/decode functions for use in research
---

# 🕵 Encoder

## hash

* Usage: `!hash`

Various hashing commands

### hash md5

* Usage: `!hash md5 <txt>`

MD5 Hash some Text

### hash sha256

* Usage: `!hash sha256 <txt>`

SHA256 Hash some Text

### hash sha1

* Usage: `!hash sha1 <txt>`

SHA1 Hash some Text

### hash sha512

* Usage: `!hash sha512 <txt>`

SHA512 Hash some Text

## encode

* Usage: `!encode`

Encode a string.

### encode b64

* Usage: `!encode b64 <message>`
* Aliases: `base64`

Encode text into base 64

### encode b16

* Usage: `!encode b16 <message>`
* Aliases: `base16`

Encode text into base 16

### encode rot

* Usage: `!encode rot <rot_key> <message>`
* Aliases: `caeser`

Encode a caeser cipher message with specified key

### encode dna

* Usage: `!encode dna <message>`

Encodes a string into DNA 4 byte ACGT format

### encode hex

* Usage: `!encode hex <message>`

Encode text into hexadecimal

### encode chr

* Usage: `!encode chr <message>`
* Aliases: `character`

Encode message into character numbers

### encode b32

* Usage: `!encode b32 <message>`
* Aliases: `base32`

Encode text into base 32

### encode braille

* Usage: `!encode braille <message>`

Encode text into braille unicode characters

### encode binary

* Usage: `!encode binary <message>`

Encode text into binary sequences of 8

## decode

* Usage: `!decode`

Decode a string.

### decode braille

* Usage: `!decode braille <message>`

Decide braille unicode characters to ascii

### decode hex

* Usage: `!decode hex <message>`

Decode a hexadecimal sequence to text

### decode chr

* Usage: `!decode chr <message>`
* Aliases: `character`

Decode character numbers to a message

### decode b32

* Usage: `!decode b32 <message>`
* Aliases: `base32`

Decode base32 text

### decode rot

* Usage: `!decode rot <rot_key> <message>`
* Aliases: `caeser`

Decode a caeser cipher message with specified key

### decode binary

* Usage: `!decode binary <message>`

Decode binary sequences of 8

### decode dna

* Usage: `!decode dna <message>`

Decodes a string of DNA in 4 byte ACGT format.

### decode b16

* Usage: `!decode b16 <message>`
* Aliases: `base16`

Decode base16 text

### decode b64

* Usage: `!decode b64 <message>`
* Aliases: `base64`

Decode base 64 text
