<div align="center">
  <img src="img/robot.webp" alt="Robot Image">
  <h1>The Large Language Model Cookbook</h1>
  <p align="center">
    🐦 <a href="https://twitter.com/charoori_ai">Follow me on Twitter</a> • 
    <!-- 💻 <a href="https://exorust.github.io/blog">Blog</a> -->
  </p>
</div>
<br/>

Welcome to the LLM Cookbook repository! This is the best collection of how to start tweaking and using and building with Large Language models. Our code is sourced from multiple places and credits are specified.

This is a compendium of the best information out there. It is organized by question.

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Setup](#setup)
- [Basic](#basic)
- [Advanced](#advanced)
- [Dataset](#dataset)
- [Deployment](#deployment)
- [Performance](#performance)
- [Tracking](#tracking)
- [Benchmarking](#benchmarking)
- [Contributions](#contributions)
- [Disclaimer](#disclaimer)

-- 

## Setup
- How to setup a GPU system?
- How to run LLM locally?
    - Olama
    - LM Studio
    - GGUF Format

## Basic
- [How to use a model for our custom data?](https://github.com/Exorust/LLM-Cookbook/blob/main/model-for-custom-data.md)
    - [How to finetune?](https://github.com/Exorust/LLM-Cookbook/blob/main/model-for-custom-data.md#how-to-finetune-a-model)
      - [FineTune Llama on HuggingFace data](https://github.com/Exorust/LLM-Cookbook/blob/main/finetuning_llama_existing_data.ipynb)
      - FineTune Llama on Custom Data
      - [FineTune Mixtral](https://github.com/Exorust/LLM-Cookbook/blob/main/mixtral_finetune.ipynb)
      - [Finetune TinyLlama](https://github.com/Exorust/LLM-Cookbook/blob/main/finetune_tinyllama.ipynb)
- How to add memory to my model? (RAG)
- How do I re-align my model? How can I apply RLHF (Reinforcement Learning from Human Feedback)?
- How do I build a Chatbot?
- [How can I prevent my model from answering wrong/malicious questions/inputs? (Validation)](https://github.com/Exorust/LLM-Cookbook/blob/main/guardrails.md)
- What kind of model should I use?
- How can I use prompting to improve my LLM output?

## Advanced
- How do I train on multiple GPUs?
- How do I build Agents?
- How to does my LLM interact with SQL?
- How does my question and answer LLM show sources to data?
- How do I make my models smaller to run on cheaper hardware? (Quantization)
- How do I merge models to improve performance?
- How do I build a mixture of experts?
- How do I reduce the size of models?
- How do I build an ocr pdf analyser?

## Dataset
- How to split documents/pdf into a dataset?
- 
- How to load a public dataset for use?
- How do I generate synthetic Data with GPT?
    - How did Alpaca do it?

## Deployment
- How do we convert a model to a REST API for consumption?
- How to we create a basic WebUI for a model?
- How do I demo my application on huggingface?


## Performance
- What kind of metrics should you be tracking?


## Tracking
- How to remember the weights and biases used?

## Benchmarking
- What are the most common benchmarks to be used?

--
## Contributions

We welcome contributions from the community! If you have a notebook, tutorial, or any valuable information related to Large Language Models, please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your contribution: `git checkout -b feature/new-contribution`.
3. Add your notebook or content to the relevant section.
4. Ensure that your notebook runs successfully and includes clear instructions.
5. Commit your changes: `git commit -m "Add new contribution: [Your Contribution Title]"`.
6. Push to the branch: `git push origin feature/new-contribution`.
7. Open a pull request, and provide a detailed description of your contribution.

Thank you for contributing to the LLM Cookbook!

---
## Disclaimer

*I am not affiliated with any sources listed here.*

---
