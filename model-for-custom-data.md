# How to do we use a model for our custom data?


- [How to do we use a model for our custom data?](#how-to-do-we-use-a-model-for-our-custom-data)
  - [Build your custom Data](#build-your-custom-data)
  - [What are the common possibilities everyone is using?](#what-are-the-common-possibilities-everyone-is-using)
  - [How to finetune a model?](#how-to-finetune-a-model)
  - [How to build a RAG pipeline?](#how-to-build-a-rag-pipeline)

## Build your custom Data


## What are the common possibilities everyone is using?
First you should try and see if you can use a pretrained model to run your application. 

## How to finetune a model?
Pre-trained models are great at generic usecases but might not solve your use case. 
Once you have picked your model you need to choose a method of fine-tuning. 
LoRA: A parameter-efficient technique (PEFT) based on low-rank adapters. Instead of training all the parameters, we only train these adapters.
QLoRA: Another PEFT based on LoRA, which also quantizes the weights of the model in 4 bits and introduce paged optimizers to manage memory spikes. Combine it with Unsloth to run it efficiently on a free Colab notebook.

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


