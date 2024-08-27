# AI Vision LLM
How much AI can see and draw? This is one of the most fascinated space that many models are trying to tackle. We have seen so many amazing results out from there. This repo attempts to achieve few things:

* Establish its own test suite with industry focus (eg. ecommerce, legal, etc)
* Provide an easy way to run tests against a list of models at the same time.
* Use LLM to evaluate test results and assign quality score.

<br>

## High level features
![](docs/ai-vision-llm-features.png)
[Source: moondream.ai](moondream.ai)

<br>

* Question/ Answer
* Object detection
* Question/ Answer
* Describe (ie. Image-to-Text)
* Text-to-Image (Generation)
* Counting

<br>

# Image-to-Text

## Demo code
This is an example repo to explore using the AI Vision model [Llava](https://developers.cloudflare.com/workers-ai/models/llava-1.5-7b-hf/) hosted on Cloudflare Workers AI. It showcase few technologies in used:

* [SvelteKit](https://kit.svelte.dev/) - javascript framework
* [Cloudflare Pages](https://pages.cloudflare.com) - hosted the demo created by this code in serverless architecture
* [Cloudflare Worker AI](https://developers.cloudflare.com/workers-ai/models/llava-1.5-7b-hf) - This demo makes use of its image-to-text model Llava-1.5-7b
<br>

## Launch Demo Over Cloudflare
* Fork this project to your own repo
* Head to https://dash.cloudflare.com > Workers & Pages > Overview > Create > Pages > Connect to Git
* Choose SvelteKit (and leave the defaults)
<br>

## Run and deploy it locally

```bash
# install
npm install

# build
npm run dev

# deploy
npm run deploy
```
<br>

## Future Vision Models To Test
* [Moondream](https://moondream.ai/playground)
* [Gemini 1.5](https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/gemini-experimental)
* [GPT-4o](https://chatgpt.com/)
* [Claude 3.5 Sonnet](https://claude.ai/)

<br>

## Leaderboard
* **VQAv2** - Question/ Answering
* **GQA** - Question/ Answering (Reasoning)
* **TextQA** - Extract Text from Images
* **TallyQA (simple)** - Counting
* **TallyQA (full)** - Counting
* **VizWiz** - 

| Model | VQAv2 | GQA | TextVQA | TallyQA (simple) | TallyQA (full) |
| --- | --- | --- | --- | --- | --- |
| LLaVA-1.5 (13.3B) | 80.0 | 63.3 | 61.3 | - | - |
| LLaVA-1.5 (7.3B) | 78.5 | 62.0 | 58.2 | - | - |
| MC-LLaVA-3B (3B) | 64.2 | 49.6 | 38.6 | - | - |
| LLaVA-Phi (3B) | 71.4 | - | 48.6 | - | - |
| moondream1 | 74.3 | 56.3 | 39.8 | - | - |
| moondream2 (latest) | 79.4 | 63.1 | 57.2 | 82.1 | 76.6 |

<br>

## Test Result

| Image | Difficulty | Model | Result |
| --- | --- | --- | --- |
| ![](test/benchmark/images/image-anime-d2.jpg) | 2 | Moondream | **What is the girl doing?**<br>The girl is sitting at a table and eating a large hamburger.<br><br>**What color is the girl's hair?**<br>The girl's hair is white. |
| ![](test/benchmark/images/product-hardware.jpg) | 3 | Moondream | **What is this?**<br>This is a computer server rack, which is a device used to store and manage multiple computer servers. The rack is filled with various computer servers, each with their own dedicated space and power supply. The servers are connected to the rack via multiple cables, indicating that they are part of a larger system. The rack is placed on a carpeted floor, and there is a couch nearby, suggesting that the setup is in a living or entertainment area.<br><br>**What is behind the stand?**<br>Behind the stand, there is a brick wall. |
| ![](test/benchmark/images/table-price-d3.png) | 3 | Gemini-1.5-flash-001 | ![](test/results/gemini/table-model-cost_result.png) |
| ![](test/benchmark/images/table-formula-d9.png) | 9 | Gemini-1.5-flash-001 | ![](test/results/gemini/table-formula-d9_result.png) |

<br>

# Text-to-Image
## Popular Models
* [Grok 2]()
* [DALL·E 3]() for an easy-to-use AI image generator
* [Midjourney](https://www.midjourney.com/explore?tab=top_month) for the best AI image results
* [pixai.art](https://pixai.art/generator/image)
* [Adobe Firefly]() for integrating AI-generated images into photos
* [DreamStudio.ai](https://dreamstudio.ai) - powered by stability.ai (ie. Stable Diffusion)
* [Leonardo.ai](https://app.leonardo.ai/) - high quality
* [Tensor.art](https://tensor.art/) - free image generation with different models and you can use it to generate images to train your model.

<br>

# References
* [HellaSwag: Understanding the LLM Benchmark for Commonsense Reasoning](https://deepgram.com/learn/hellaswag-llm-benchmark-guide)
* [Youtube: TensortArt + Flux Training : Train FLUX-1 for FREE with Custom Images!](https://www.youtube.com/watch?v=5pcBOJ0xsRw)
* [An In-Depth Look at Elo and MMLU Scores for Leading Language Models](https://medium.com/tr-labs-ml-engineering-blog/guidelines-for-evaluating-large-language-models-3d57ba76656a)



