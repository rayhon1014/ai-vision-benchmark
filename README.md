# AI Vision LLM
How much AI can see and draw? This is one of the most fascinated space that many models are trying to tackle. We have seen so many amazing results out from there. This repo is aim to test them out and see if we can apply what they are capable of in the industry for public usage.

## High level features
![](docs/ai-vision-llm-features.png)
<br>
* Question/ Answer
* Object detection
* Question/ Answer
* Describe (ie. Image-to-Text)
* Text-to-Image
* Counting

<br>

# Test out Llava over Cloudflare Worker AI

This is an example repo to explore using the AI Vision model [Llava](https://developers.cloudflare.com/workers-ai/models/llava-1.5-7b-hf/) hosted on Cloudflare Workers AI.

This is a [SvelteKit](https://kit.svelte.dev/) app hosted on [Pages](https://pages.cloudflare.com).


[<img src="https://img.youtube.com/vi/MLbo7MGY_lU/0.jpg">](https://youtu.be/MLbo7MGY_lU "AI Can See Clearly Now - YouTube walkthrough")
<br>

## Use the Template

Press the Use Template button on GitHub
Create a new repository in your account.
Head to https://dash.cloudflare.com > Workers & Pages > Overview > Create > Pages > Connect to Git
Choose SvelteKit (and leave the defaults)

---

OR

---

## Run and deploy it locally

```bash
# imstall
npm install

# build
npm run dev

# deploy
npm run dev
```
<br>

# Other Vision Models
* [Moondream](https://moondream.ai/playground), [Github](https://github.com/vikhyat/moondream/blob/main/README.md)
* [Gemini](https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/gemini-experimental)
- [GPT-4o]
- [Claude]
- [LLaVA-1.5]

<br>

# Benchmarks

| Model | VQAv2 | GQA | TextVQA | TallyQA (simple) | TallyQA (full) |
| --- | --- | --- | --- | --- | --- |
| moondream1 | 74.7 | 57.9 | 35.6 | - | - |
| **moondream2** (latest) | 79.4 | 63.1 | 57.2 | 82.1 | 76.6 |

<br>

## Test Result

| Image | Model | Result |
| --- | --- | --- |
| ![](test/benchmark/images/image-anime-d2.jpg.jpg) | Moondream | **What is the girl doing?**<br>The girl is sitting at a table and eating a large hamburger.<br><br>**What color is the girl's hair?**<br>The girl's hair is white. |
| ![](test/benchmark/images/product-hardware.jpg) | Moondream | **What is this?**<br>This is a computer server rack, which is a device used to store and manage multiple computer servers. The rack is filled with various computer servers, each with their own dedicated space and power supply. The servers are connected to the rack via multiple cables, indicating that they are part of a larger system. The rack is placed on a carpeted floor, and there is a couch nearby, suggesting that the setup is in a living or entertainment area.<br><br>**What is behind the stand?**<br>Behind the stand, there is a brick wall. |
| ![](test/benchmark/images/table-price-d3.png) | Gemini-1.5-flash-001 | ![](test/results/gemini/table-model-cost_result.png) |
| ![](test/benchmark/images/table-formula-d9.png) | Gemini-1.5-flash-001 | ![](test/results/gemini/table-formula-d9_result.png) |

# Image Generation
* [Grok 2]()
* [DALL·E 3]() for an easy-to-use AI image generator
* [Midjourney](https://www.midjourney.com/explore?tab=top_month) for the best AI image results
* [pixai.art](https://pixai.art/generator/image)
* [Adobe Firefly]() for integrating AI-generated images into photos
* [DreamStudio.ai](https://dreamstudio.ai) - powered by stability.ai (ie. Stable Diffusion)
* [Leonardo.ai](https://app.leonardo.ai/) - high quality

## Dreamstudio.ai
* DreamStudio (Stable Diffusion's web app) is the only major AI picture generator that still offers free credits. 
* The app is incredibly affordable and customizable; super powerful with generally great results
* Stable diffusion is open source
* Pricing: $1 per 100 credits (~500 images)
![](docs/dreamstudio.png)

## Adobe Firefly

# Character Consistency