---
description: Generate amazing art using artificial intelligence!
---

# 🎨 Generative AI

## wombo

* Usage: `!wombo <arguments>`
* Aliases: `draw, text2art, text2img, and text2image`

Generate art using Wombo.\
\
If you would like to view the styles available, run !wombo --styles.\
\
**Arguments:**\
prompt The prompt to use for the art.\
\--style The style to use for the art. Defaults to Realistic v2.\
\--image The image to use for the art. You can also upload an attachment instead of using this argument.\
\--amount The amount of images to generate.\
\--width The width of the art. Defaults to 1024. Range is 100-10000\
\--height The height of the art. Defaults to 1024. Range is 100-10000\
\--steps The amount of steps to use for the art. Defaults to 40. Range is 20-50.\
\--text-cfg The text cfg value to use for the art. Defaults to 7.5. Range is 1-30.\
\--negative The negative prompt to use for the art. Defaults to None.\
\--seed The seed to use for the art. Defaults to None.\
\
**Note: If the total amount of pixels is greater than 35,000,000, it will return one image.**

## anything

* Usage: `!anything <args>`
* Checks: `is_nsfw`

Generate art using the Anything v4.5 model.\
\
**Arguments:**\
prompt: The prompt to use for the art.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## aom

* Usage: `!aom <args>`
* Checks: `is_nsfw`

Generate art using the AOM3 model.\
\
**Arguments:**\
prompt: The prompt to use for the art.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## counterfeit

* Usage: `!counterfeit <args>`
* Checks: `is_nsfw`

Generate art using the Counterfeit v2.5 model.\
\
**Arguments:**\
prompt: The prompt to use for the art.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## nemu

* Usage: `!nemu <args>`
* Checks: `is_nsfw`

Generate art using the Nemu model.\
\
**Arguments:**\
prompt: The prompt to use for the art.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.
