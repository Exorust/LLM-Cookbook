# How to do we use a model for our custom data?

You would need your own data to be processed. You would need to try to test out an existing pre-trained model and see if it does a good job. Then you would try to fine-tune the chosen model and possibly add an RAG pipeline to ensure it does a good job. Post which you would add guardrails to ensure that your model is producing the correct output.

- [How to do we use a model for our custom data?](#how-to-do-we-use-a-model-for-our-custom-data)
  - [Load your custom Data](#load-your-custom-data)
  - [What are the common possibilities everyone is using?](#what-are-the-common-possibilities-everyone-is-using)
  - [How to finetune a model?](#how-to-finetune-a-model)
  - [How to build a RAG pipeline?](#how-to-build-a-rag-pipeline)
  - [How to add Guardrails?](#how-to-add-guardrails)

## Load your custom Data
Follow the recipies shown here: https://github.com/Exorust/LLM-Cookbook/blob/main/README.md#Dataset


## What are the common possibilities everyone is using?
First you should try and see if you can use a pretrained model to run your application. 

## How to finetune a model?
Pre-trained models are great at generic usecases but might not solve your use case. 
Once you have picked your model you need to choose a method of fine-tuning. 
- [LoRA](https://arxiv.org/abs/2106.09685): A parameter-efficient technique (PEFT) based on low-rank adapters. Instead of training all the parameters, we only train these adapters.
- [QLoRA](https://arxiv.org/abs/2305.14314): Another PEFT based on LoRA, which also quantizes the weights of the model in 4 bits and introduce paged optimizers to manage memory spikes. Combine it with Unsloth to run it efficiently on a free Colab notebook.

Best tools for Finetuning:
- Unsloth: Allows you to train on Collab easily
- Axolotl: Easy tool for local fine-tuning
- DeepSpeed: Efficient fine-tuning on multi-gpu Setup

Our Notebooks to guide you:
- FineTune Llama on HuggingFace data
- FineTune Llama on Own Data
- FineTune Mixtral
- Finetune TinyLlama 

Good resources:
- [Brev Notebooks for Finetuning Models](https://github.com/brevdev/notebooks)

## How to build a RAG pipeline?
Follow the recipies shown here: https://github.com/Exorust/LLM-Cookbook/blob/main/memory-rag.md#

## How to add Guardrails?
Follow the recipies shown here: https://github.com/Exorust/LLM-Cookbook/blob/main/guardrails.md#