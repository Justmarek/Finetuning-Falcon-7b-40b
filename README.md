# Finetuning-Falcon-7b-40b
In this notebook we will finetune Falcon 7b/40b instruct to generate high quality Midjourney prompts. 

## Introduction
Quite often stakeholders might want "GPT, but for my specific use case". There are generally 2 approaches to this problem:

1. Fine-tuning large language models (LLMs) - retrain a large langauge model with private data
2. Knowledge base embedding - you are creating a vector database or embedding of your knowledge and you try and find the relevant data and feed it into your large langauge model 

## What is the difference between these approaches?
1. Fine-tuning LLMs - is good for making models behave a certain way or maybe digitising someone. You can feed in transcripts, podcasts and their general language and make them behave like someone e.g Talk like Boris Johnson
2. Knowledge base embedding - is good when you have lots of domain knowledge and want to query it and have it as an output of your model e.g Knowledge about insurance markets

Generally using a knowledge based embedding or retrieval augmented generation (RAG), is the correct approach when a stakeholder asks you for "GPT, but for my specific use case". However in this case we are going to try out fine-tuning [Falcon 7b/40b](https://huggingface.co/tiiuae/falcon-7b) for creating [Midjourney](https://docs.midjourney.com/docs/model-versions) prompts. 

## What do I want to do?
I want my model to take a simple prompt like: "Midjourney prompt for a fantasy village night" and turn it into something better like "a beautiful adorable fantasy village the ground is lit like warm daylight, but the sky is dark and full of stars --ar 16:9"   

## What data an I fine-tune using?
You can finetune your model using your own datasets, or publically available datasets, such as those found on [Kaggle](Kaggle.com) or [Huggingface](https://huggingface.co/docs/datasets/index). Fine-tuning can be started using limited amounts of data, be it 100s or 1000s of rows, but as always generally the more data you have the better. 

# How do you run this notebooks?

1. You can run it on [Google Colab](https://colab.research.google.com/drive/1IqL0ay04RwNNcn5R7HzhgBqZ2lPhHloh?usp=sharing)
2. You need a HuggingFace API key, which you can get from your HuggingFace account.

   
