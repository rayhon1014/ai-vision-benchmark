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

# Demo Code

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

# Other Vision Models
* [Moondream](https://moondream.ai/playground), [Github](https://github.com/vikhyat/moondream/blob/main/README.md)
* [Gemini](https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/gemini-experimental)
- [GPT-4o]
- [Claude]
- [LLaVA-1.5]

<br>

# Vision LLM Benchmarks
* **VQAv2** - Question/ Answering
* **GQA** - Question/ Answering (Reasoning)
* **TextQA** - Extract Text from Images
* **TallyQA (simple)** - Counting
* **TallyQA (full)** - Counting
* **VizWiz** 

| Model | VQAv2 | GQA | TextVQA | TallyQA (simple) | TallyQA (full) |
| --- | --- | --- | --- | --- | --- |
| LLaVA-1.5 (13.3B) | 80.0 | 63.3 | 61.3 | - | - |
| LLaVA-1.5 (7.3B) | 78.5 | 62.0 | 58.2 | - | - |
| MC-LLaVA-3B (3B) | 64.2 | 49.6 | 38.6 | - | - |
| LLaVA-Phi (3B) | 71.4 | - | 48.6 | - | - |
| moondream1 | 74.3 | 56.3 | 39.8 | - | - |
| moondream2 (latest) | 79.4 | 63.1 | 57.2 | 82.1 | 76.6 |

<br>

# General LLM Benchmark
These are the most commonly utilized LLM Benchmarks among models’ technical reports:

* **MMLU** - Multitask accuracy
* **HellaSwag** - Reasoning
* **HumanEval** - Python coding tasks
* **BBHard** - Probing models for future capabilities
* **GSM-8K** - Grade school math
* **MATH** - Math problems with 7 difficulty levels

![](docs/llm-benchmark2.png)

## GPQA (General Purpose Question Answering)
**What it Tests:** GPQA benchmarks measure a model's ability to answer a wide range of general-purpose questions. These can include questions from various domains, including common knowledge, current events, and specialized fields.<br><br>
**Key Skills Tested:** General knowledge, reasoning, language understanding, and context comprehension.<br><br>

## MMLU (Massive Multitask Language Understanding)
**What it Tests:** MMLU evaluates a model's ability to perform across a diverse set of language-based tasks. It includes questions from 57 different subjects, covering everything from elementary mathematics to advanced science topics.<br><br>
**Key Skills Tested:** Multitask learning, subject-specific knowledge, language understanding.<br><br>

## MMLU-Pro
**What it Tests:** MMLU-Pro is an enhanced benchmark designed to evaluate the language understanding capabilities of LLMs across a broader and more challenging set of tasks. It builds upon the original Massive Multitask Language Understanding (MMLU) dataset by addressing several limitations and introducing new features to increase the difficulty and robustness of the evaluation..<br><br>
**Key Skills Tested:** Advanced subject-specific knowledge, professional-level reasoning.<br><br>

## HellaSwag (Sentence Completion)
**What it Tests:** HellaSwag is a challenge dataset for evaluating commonsense NLI that is specially hard for state-of-the-art models, though its questions are trivial for humans (>95% accuracy)<br><br>
**Key Skills Tested:** The main goal of HellaSwag is to evaluate whether AI models can apply commonsense reasoning to understand and predict outcomes in various scenarios, making it a crucial benchmark for assessing the depth of understanding and reasoning capabilities in natural language processing (NLP) models.


## MATH
**What it Tests:** MATH is a new dataset of 12,500 challenging competition mathematics problems. Each problem in MATH has a full step-by-step solution which can be used to teach models to generate answer derivations and explanations.<br><br>
**Key Skills Tested:** Numerical reasoning, problem-solving, symbolic manipulation, and mathematical logic.<br><br>
**Leaderboard**: https://paperswithcode.com/sota/math-word-problem-solving-on-math

## HumanEval (Python Coding Tasks)
**What it Tests:** It consists of 164 original programming problems, assessing language comprehension, algorithms, and simple mathematics, with some comparable to simple software interview questions.<br><br>
**Key Skills Tested:** Coding ability, syntax understanding, logical problem-solving, and programming language fluency.<br><br>
**Leaderboard**: https://paperswithcode.com/sota/code-generation-on-humaneval

## MMMU
**What it Tests:** a new benchmark designed to evaluate multimodal models on massive multi-discipline tasks demanding college-level subject knowledge and deliberate reasoning. MMMU includes 11.5K meticulously collected multimodal questions from college exams, quizzes, and textbooks, covering six core disciplines: Art & Design, Business, Science, Health & Medicine, Humanities & Social Science, and Tech & Engineering. These questions span 30 subjects and 183 subfields, comprising 30 highly heterogeneous image types, such as charts, diagrams, maps, tables, music sheets, and chemical structures.<br><br>
**Key Skills Tested:** MMMU is designed to measure three essential skills in LMMs: perception, knowledge, and reasoning.<br><br>
![](https://mmmu-benchmark.github.io/static/images/mmlu_example.Jpeg)

## MathVista
**What it Tests:** MathVista seems to be another benchmark focused on mathematics, potentially with a focus on more visualization-based or application-based mathematical tasks.<br><br>
**Key Skills Tested:** Applied mathematics, problem-solving with visual components, and mathematical reasoning.<br><br>

## DocVQA
**What it Tests:** DocVQA benchmarks evaluate how well a model can answer questions based on the content of documents. This typically involves understanding text within complex layouts, tables, forms, and scanned documents.<br><br>
**Key Skills Tested:** Document understanding, OCR (Optical Character Recognition), text comprehension, and information extraction.<br><br>


<br>

# Test Result

| Image | Difficulty | Model | Result |
| --- | --- | --- | --- |
| ![](test/benchmark/images/image-anime-d2.jpg) | 2 | Moondream | **What is the girl doing?**<br>The girl is sitting at a table and eating a large hamburger.<br><br>**What color is the girl's hair?**<br>The girl's hair is white. |
| ![](test/benchmark/images/product-hardware.jpg) | 3 | Moondream | **What is this?**<br>This is a computer server rack, which is a device used to store and manage multiple computer servers. The rack is filled with various computer servers, each with their own dedicated space and power supply. The servers are connected to the rack via multiple cables, indicating that they are part of a larger system. The rack is placed on a carpeted floor, and there is a couch nearby, suggesting that the setup is in a living or entertainment area.<br><br>**What is behind the stand?**<br>Behind the stand, there is a brick wall. |
| ![](test/benchmark/images/table-price-d3.png) | 3 | Gemini-1.5-flash-001 | ![](test/results/gemini/table-model-cost_result.png) |
| ![](test/benchmark/images/table-formula-d9.png) | 9 | Gemini-1.5-flash-001 | ![](test/results/gemini/table-formula-d9_result.png) |


# Price
## Gemini
![](docs/gemini-pricing.png)
<br>

# Image Generation
* [Grok 2]()
* [DALL·E 3]() for an easy-to-use AI image generator
* [Midjourney](https://www.midjourney.com/explore?tab=top_month) for the best AI image results
* [pixai.art](https://pixai.art/generator/image)
* [Adobe Firefly]() for integrating AI-generated images into photos
* [DreamStudio.ai](https://dreamstudio.ai) - powered by stability.ai (ie. Stable Diffusion)
* [Leonardo.ai](https://app.leonardo.ai/) - high quality
* [Tensor.art](https://tensor.art/) - free image generation with different models and you can use it to generate images to train your model.

## Dreamstudio.ai
* DreamStudio (Stable Diffusion's web app) is the only major AI picture generator that still offers free credits. 
* The app is incredibly affordable and customizable; super powerful with generally great results
* Stable diffusion is open source
* Pricing: $1 per 100 credits (~500 images)
![](docs/dreamstudio.png)

## Adobe Firefly

# Character Consistency
