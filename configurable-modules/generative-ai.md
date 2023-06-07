---
description: Generate amazing art using artificial intelligence!
---

# 🎨 Generative AI

Generate incredible art using AI.

## wombo

* Usage: `!wombo <arguments>`
* Aliases: `draw, text2art, text2img, and text2image`

Generate art using Wombo.\
\
If you would like to view the styles available, run !wombo --styles.\
\
**Arguments:**\
\- prompt The prompt to use for the art.\
\- --style The style to use for the art. Defaults to Realistic v2.\
\- --image The image to use for the art. You can also upload an attachment instead of using this argument.\
\- --amount The amount of images to generate.\
\
These arguments may or may not be available depending on if the bot is using the official or app API.\
\- --width The width of the art. Defaults to 1024. Range is 100-10000\
\- --height The height of the art. Defaults to 1024. Range is 100-10000\
\- Note: If the total amount of pixels is greater than 35,000,000, it will return one image.\
\--steps The amount of steps to use for the art. Defaults to 40. Range is 20-50.\
\--text-cfg The text cfg value to use for the art. Defaults to 7.5. Range is 1-30.\
\--negative The negative prompt to use for the art. Defaults to None.\
\--seed The seed to use for the art. Defaults to None.

## magicprompt

* Usage: `!magicprompt <prompt>`
* Aliases: `enhanceprompt and betterprompt`

Generate a prompt using MagicPrompt.\
\
**Arguments:**\
\- prompt The prompt to use for the art.

## waifudiffusion

* Usage: `!waifudiffusion <text>`

Generate art using Waifu Diffusion.

## upscale

* Usage: `!upscale [link=None]`

Upscale an image.\
\
If no URL is provided, the bot the first image in the message.

## anything

* Usage: `!anything <args>`

Generate art using the Anything v4.5 model.\
\
Warning: This model has a high likelihood of generating NSFW content (it will still be behind the NSFW filter.)\
\
Arguments:\
prompt: The prompt to use for the model.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## aom

* Usage: `!aom <args>`

Generate art using the AOM3 model.\
\
Warning: This model has a high likelihood of generating NSFW content (it will still be behind the NSFW filter.)\
\
Arguments:\
prompt: The prompt to use for the model.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## counterfeit

* Usage: `!counterfeit <args>`

Generate art using the Counterfeit v2.5 model.\
\
Warning: This model has a high likelihood of generating NSFW content (it will still be behind the NSFW filter.)\
\
Arguments:\
prompt: The prompt to use for the model.\
\--negative: The negative prompt to use for the model.\
\--cfg-scale: The cfg scale to use for the model. This is a number between 1 and 10, inclusive.\
\--denoising-strength: The denoising strength to use for the model. This is a number between 0 and 1, inclusive.

## latentdiffusion

* Usage: `!latentdiffusion <text>`

Generate art using Latent Diffusion.

## craiyon

* Usage: `!craiyon <text>`

Generate art using Craiyon.\
\
The only argument is the text to generate the image from.
