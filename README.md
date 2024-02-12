<div align="center">
  <img src="img/robot.webp" alt="Robot Image">
  <h1>The Large Language Model Cookbook</h1>
  <p align="center">
    🐦 <a href="https://twitter.com/charoori_ai">Follow me on Twitter</a> 
    📧 <a href="mailto:chandrahas.aroori@gmail.com?subject=LLM%20Cookbook">Contact on Email</a>
  </p>
</div>
<br/>

Welcome to the evolving LLM Cookbook repository! This space is dedicated to becoming the ultimate guide for anyone interested in tweaking, using, and building with Large Language Models. Our repository is a growing collection, sourced from diverse places, with all credits duly acknowledged.

Consider this compendium as your go-to resource, meticulously organized by questions to help you navigate the vast world of LLMs with ease. We're on a mission to compile the best information out there, and we invite the community to contribute. Whether you have insights, code, or questions, your input is invaluable in enriching this repository. Join us in shaping the LLM Cookbook into an even more comprehensive resource for all!

### Table of Contents
- [Setup](#setup)
- [Basic](#basic)
- [Advanced](#advanced)
- [Multi-modal](#multi-modal)
- [Dataset](#dataset)
- [Deployment](#deployment)
- [Performance](#performance)
- [Tracking](#tracking)
- [Benchmarking](#benchmarking)
- [Contributions](#contributions)
- [Disclaimer](#disclaimer)



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

## Multi-modal


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

This cookbook contains code snippets, examples, and techniques gathered from various sources, including but not limited to online repositories, public domain resources, and contributions from the coding community. The inclusion of such code is intended for educational purposes and as a resource for professionals seeking to enhance their programming skills. While we have made every effort to credit the original authors and ensure the accuracy and reliability of the information presented, we cannot guarantee the validity of all code segments or their applicability to specific projects or environments.

Users of this cookbook are encouraged to review and test code thoroughly before integration into production environments. The authors and publishers of this cookbook disclaim any liability for errors, omissions, or the suitability of any code for particular applications. Furthermore, the technology landscape is dynamic, and practices, tools, and code standards evolve over time. Therefore, readers are advised to consult current documentation and resources to ensure best practices are followed.

For specific code contributions, source attributions have been provided where possible. We acknowledge the collective knowledge of the programming community and express our gratitude to those who openly share their work. If you believe any code has been used inappropriately or without proper authorization, please contact us for review and corrective action.

Use of the code provided within this cookbook is at your own risk. No warranty, express or implied, is made regarding the effectiveness, compatibility, or safety of the code samples. By using the information contained herein, you agree to assume all risks associated with such use, including but not limited to the loss of data, system failure, or financial losses.

---
