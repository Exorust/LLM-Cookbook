<div align="center">
  <img src="img/robot.webp" alt="Robot Image">
  <h1>The Large Language Model Cookbook</h1>
  <p align="center">
    🐦 <a href="https://twitter.com/charoori_ai">Follow me on Twitter</a> •
    📧 <a href="mailto:chandrahas.aroori@gmail.com?subject=LLM%20Cookbook">Contact on Email</a>
  </p>
</div>
<br/>

Welcome to the evolving LLM Cookbook repository! This space is dedicated to becoming the ultimate guide for anyone interested in tweaking, using, and building with Large Language Models. Our repository is a growing collection, sourced from diverse places, with all credits duly acknowledged.

Consider this compendium as your go-to resource, meticulously organized by questions to help you navigate the vast world of LLMs with ease. We're on a mission to compile the best information out there, and we invite the community to contribute. Whether you have insights, code, or questions, your input is invaluable in enriching this repository. Join us in shaping the LLM Cookbook into an even more comprehensive resource for all!

### Table of contents
- [Model Creation](#model-creation)
  - [Setup](#setup)
  - [Basic](#basic)
  - [Advanced](#advanced)
  - [Reinforcement Learning from Human Feedback](#reinforcement-learning-from-human-feedback)
  - [Quantization](#quantization)
  - [Agents](#agents)
  - [Multi-modal](#multi-modal)
    - [Vision Models](#vision-models)
  - [Datasets](#datasets)
- [LLMOps / MLOps](#llmops--mlops)
  - [Deployment](#deployment)
  - [Monitoring](#monitoring)
  - [Speed](#speed)
  - [Performance](#performance)
  - [Tracking](#tracking)
  - [Benchmarking / Model Evaluation](#benchmarking--model-evaluation)
- [Use Case Recipes](#use-case-recipes)
- [Contributions](#contributions)
- [Disclaimer](#disclaimer)


## Model Creation

### Setup

- How to setup a GPU system?
- How to run LLM locally?
  - [Olama](https://github.com/ollama/ollama)
  - [LM Studio](https://lmstudio.ai/)
- How to run LLMs on Cloud Providers? **(No affiliation with any of them)**
  - [LambdaLabs](https://lambdalabs.com/)
  - [RunPod](https://www.runpod.io)
  - [Brev.dev](https://brev.dev/)
  - [Lightning.ai](https://lightning.ai)

### Basic

- [How to use a model for our custom data?](https://github.com/Exorust/LLM-Cookbook/blob/main/model-for-custom-data.md)
  - [How to finetune?](https://github.com/Exorust/LLM-Cookbook/blob/main/model-for-custom-data.md#how-to-finetune-a-model)
    - [FineTune Llama on HuggingFace data](https://github.com/Exorust/LLM-Cookbook/blob/main/finetuning_llama_existing_data.ipynb)
    - [FineTune Mixtral](https://github.com/Exorust/LLM-Cookbook/blob/main/mixtral_finetune.ipynb)
    - [Finetune TinyLlama](https://github.com/Exorust/LLM-Cookbook/blob/main/finetune_tinyllama.ipynb)
    - [Generic Guide to FineTuning](https://rentry.org/llm-training)
- [How to add memory to my model? (RAG)](https://github.com/Exorust/LLM-Cookbook/blob/main/memory.md)
  - [How to implement RAG?](https://github.com/Exorust/LLM-Cookbook/blob/main/langchain-qa-rag.ipynb)
  - [How can I use a hosted Vector Database for my Model Memory?](https://github.com/Exorust/LLM-Cookbook/blob/main/hosted-rag.md)
- [How do I re-align my model? How can I apply RLHF (Reinforcement Learning from Human Feedback)?](https://github.com/Exorust/LLM-Cookbook/blob/main/README.md#reinforcement-learning-from-human-feedback)
- How do I build a Chatbot?
- [How can I prevent my model from answering wrong/malicious questions/inputs? (Validation)](https://github.com/Exorust/LLM-Cookbook/blob/main/guardrails.md)
- What kind of model should I use?
- How can I use prompting to improve my LLM output?
- How do I integrate API's into my LLM?

### Advanced

- [How to improve efficiency of training on a single GPU?](https://huggingface.co/docs/transformers/perf_train_gpu_one)
- [How do I train on multiple GPUs?](https://github.com/Exorust/LLM-Cookbook/blob/main/multi-gpu.md)
  - [DeepSpeed](https://github.com/microsoft/DeepSpeed)
- [How does my LLM interact with SQL?](https://github.com/Exorust/LLM-Cookbook/blob/main/sql-integ.ipynb)
- How does my LLM show sources to data? (Citations)
- How do I merge models to improve performance?
- How do I build a mixture of experts?
- How do I reduce the size of models?
- How build Positional Embeddings?

### Reinforcement Learning from Human Feedback
- How to create my own Preference Dataset?
- [How to use DPO to train my own LLM?](https://huggingface.co/blog/dpo-trl)
- [How to train Llama with RLHF? (PPO older method)](https://huggingface.co/blog/stackllama)

### Quantization

- [How much memory will my model consume?](https://blog.eleuther.ai/transformer-math/)
- How do I make my models smaller to run on cheaper hardware? (Quantization)

### Agents

- How do I build Agents?

### Multi-modal
#### Vision Models

### Datasets

- [How to load a public dataset for use?](https://github.com/Exorust/LLM-Cookbook/blob/main/load-dataset.md)
- [How to load data from a database?](https://github.com/Exorust/LLM-Cookbook/blob/main/dataset-database.md)
- How can I upload my own dataset to HuggingFace?
- [How to build a standard Question Answer Dataset for LLMs?](https://wandb.ai/capecape/alpaca_ft/reports/How-to-Fine-Tune-an-LLM-Part-1-Preparing-a-Dataset-for-Instruction-Tuning--Vmlldzo1NTcxNzE2)
- [Where can I find datasets for LLM training?](https://github.com/Zjh-819/LLMDataHub)
- [How to clean my own synthetic Dataset?](https://github.com/AlpinDale/gptslop)
- [How to pad my data for Causal LM?](https://towardsdatascience.com/padding-large-language-models-examples-with-llama-2-199fb10df8ff)
- How to split documents/pdf into a dataset?
- How do I generate synthetic Data with GPT?
- How to remove duplicates in your dataset? (dedup)

## LLMOps / MLOps

### Deployment

- [How do we convert a model to a REST API for consumption?](https://github.com/Exorust/LLM-Cookbook/blob/main/deployment.md)
- How to compile the model to multiple run systems?
  - GGUF
  - GPTQ
  - EXL2
  - AWQ
  - HQQ
- How to host a LLM model on a cloud?
- How do we create a basic WebUI for a model?
- How do I demo my application on huggingface?
- How to run LLMs on multiple platforms?
  - How to convert LLMs to ONNX?
- How to build an on-prem system to run LLMs?
- How to reduce inference cost?

### Monitoring

- [How to monitor your LLM?](https://github.com/Exorust/LLM-Cookbook/blob/main/monitor.md)
- How to monitor the LLM consistency in output quality?
- How to run test cases for LLMs?
  - Langsmith
  - DeepEval

### Speed

- How to decrease latency of the LLM models?
- How to increase speed of inference of LLM Models?
  - vLLM
  - ExLlamaV2
  - TensorRT: Speed
- How to increase speed of training of LLM Models?
  - How do I train on multiple GPUs?
  - DeepSpeed: Increase Training Phase
- Tensor Compilers
  - [List of Tensor compilers: Github](https://github.com/merrymercy/awesome-tensor-compilers#open-source-projects)


### Performance

- What kind of metrics should you be tracking?

### Tracking

- [How do I track the experiments done & best results?](https://github.com/Exorust/LLM-Cookbook/blob/main/track.md)

### Benchmarking / Model Evaluation
- How do traditional NLP metrics translate to LLMs?
  - [Perplexity](https://huggingface.co/docs/transformers/perplexity)
  - BLEU
- What are the most common benchmarks to be used?
  - [Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
  - [Big Bench](https://github.com/google/BIG-bench)
- How to define task-specific benchmarks?
- [How to capture acceptance of answers by the users?](https://docs.smith.langchain.com/cookbook/feedback-examples)
- How to get Human evaluation benchmarks?

## Use Case Recipes

- How to build a 'talk-to-your-data' application?
- How do I build an ocr pdf analyser?
- How to build a chatbot on internal documentation?
- How to build a conversational chatbot from Database information?
- How to use a LLMs for Medical Data?
  - How to build LLMs for teaching Medicine?
  - How to train LLMs to understand Medical Data?

---

## Contributions

We're excited to invite the community to contribute! If you've got insights, notebooks, or tutorials that could enrich our understanding or utilization of Large Language Models, here's how you can share your knowledge:

Before starting, ensure your contribution is focused on providing solutions to specific use cases rather than merely elucidating methods. For clarity:
- "What is model quantization?" is not. ❌
- "How to reduce the size of a model?" is encouraged. ✅

To contribute, please follow these steps:

1. Fork the project repository.
2. Utilize the `template.md` file to craft a new markdown document.
3. Incorporate your document's details and link it within the `README`.
4. Confirm that your notebook operates smoothly and includes straightforward instructions.
5. Initiate a new branch for your work with: `git checkout -b feature/new-contribution`.
6. Record your modifications with: `git commit -m "Add new contribution: [Title of Your Contribution]"`.
7. Upload your changes to the branch: `git push origin feature/new-contribution`.
8. Propose a pull request, ensuring you offer a comprehensive description of what you're introducing.

Your involvement enriches the LLM Cookbook—thank you for your participation!

---

## Disclaimer

This cookbook contains code snippets, examples, and techniques gathered from various sources, including but not limited to online repositories, public domain resources, and contributions from the coding community. The inclusion of such code is intended for educational purposes and as a resource for professionals seeking to enhance their programming skills. While we have made every effort to credit the original authors and ensure the accuracy and reliability of the information presented, we cannot guarantee the validity of all code segments or their applicability to specific projects or environments.

Users of this cookbook are encouraged to review and test code thoroughly before integration into production environments. The authors and publishers of this cookbook disclaim any liability for errors, omissions, or the suitability of any code for particular applications. Furthermore, the technology landscape is dynamic, and practices, tools, and code standards evolve over time. Therefore, readers are advised to consult current documentation and resources to ensure best practices are followed.

For specific code contributions, source attributions have been provided where possible. We acknowledge the collective knowledge of the programming community and express our gratitude to those who openly share their work. If you believe any code has been used inappropriately or without proper authorization, please contact us for review and corrective action.

Use of the code provided within this cookbook is at your own risk. No warranty, express or implied, is made regarding the effectiveness, compatibility, or safety of the code samples. By using the information contained herein, you agree to assume all risks associated with such use, including but not limited to the loss of data, system failure, or financial losses.

---
