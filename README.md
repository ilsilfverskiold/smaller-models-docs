# Transformers-NLP-Docs

Documentation and practical guides for working with and fine-tuning smaller open-source transformer models using the Hugging Face platform and the transformers library. Documentation on models include base-models, sizes, tasks and usual business use cases. 

**Note:** At the moment there are only cook books in this repo for fine-tuning encoder and seq-to-seq models. 

## Intro

I've split the repo into a **'docs'** and **'cook'** part where the **'docs'** part have info on the three models types, encoder, decoder and seq2seq. It also has info on the different base-models you can use, what organisation they come from, their tasks, different fine-tuned models that are open-source in the Hugging Face library and a page dedicated specifically to what business cases each model and task can do well in. 

The **'cook'** part of this repo hands you the notebooks that will allow you to work with datasets, fine-tune smaller models based on their architecture and how to use the models with the Hugging Face pipeline.

If you're new to fine-tuning smaller NLP models check out this intro [here](https://medium.com/gitconnected/fine-tune-smaller-nlp-models-with-hugging-face-for-specific-use-cases-1745813471dc) that goes through fine-tuning a BART (seq2seq model).

## Contents

- [Docs](#docs)
  - [Models](#models)
  - [Business Cases](#business-cases)
- [Cook](#cook)
  - [Datasets](#datasets)
  - [Fine-Tune](#fine-tune)
  - [Using](#using)
  - [Creating Datasets](#create-dataset)

## Docs
Documentation on the different architectures, their base models, tasks and where it makes sense to fine-tune them. Also various examples of fine-tuned models from Hugging Face as examples.

### Models
Detailed documentation on different transformer model architectures and different fine-tuned models you can find in Hugging Face.
- [Decoder](./docs/models/decoder.md)
- [Encoder](./docs/models/encoder.md)
- [Seq-to-Seq](./docs/models/seq-to-seq.md)

### Business-Cases
Brainstorm typical ideas for different business cases for each task and architecture.
- [Decoder](./docs/business-cases/decoder.md)
- [Encoder](./docs/business-cases/encoder.md)
- [Seq-to-Seq](./docs/business-cases/seq-to-seq.md)

## Cook
Cook books for fine-tuning, preprocessing datasets and using the models in an application.

### Datasets
Cook books for processing and importing different datasets in Colab to use for fine-tuning or pushing to Hugging Face's dataset's library. If you're looking for a completely guide see the **'fine-tune'** section or folder directly.
- Process Custom Dataset
  - Guide on how to process a custom dataset
  - File: [process_custom_dataset.ipynb (Notebook)](./cook/datasets/process_custom_dataset.ipynb)
  - Notes: this will be connecting to a csv file located in your Google Drive. We're importing it and then splitting it up to a training, testing and validation set.
- Process Hugging Face Dataset
  - Guide on how to process a custom dataset
  - File: [process_huggingface_dataset.ipynb (Notebook)](./cook/datasets/process_huggingface_dataset.ipynb)
  - Notes: this will be importing a dataset located in Hugging Face, then setting a validation set from the training set (as it is missing), doing some slight filtering which is optional.
- Push Custom Dataset to Hugging Face
  - Instructions on how to push a custom dataset to the Hugging Face hub.
  - File: [push_custom_dataset_huggingface.ipynb (Notebook)](./cook/datasets/push_custom_dataset_huggingface.ipynb)
  - Notes: this script imports a csv file from Google Drive, creates a dataset dict and then pushes it to the Hugging Face hub where you can share it with others (or keep it private).

### Fine-Tune
Cook books for the entire fine-tune process. At the moment only has cook books for fine-tuning a seq-to-seq model and encoder models for text classification.

**Seq-to-Seq** Models
- Fine Tune **Seq-to-Seq** Model with Custom Dataset
  - Step by step script for fine-tuning Seq-to-Seq models using custom datasets.
  - File: [fine_tune_encoder_custom_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_seqtoseq_custom_dataset.ipynb)
  - Notes: dataset is smaller (8,500 rows) will be imported from Google Drive
- Fine Tune **Seq-to-Seq** with Hugging Face Dataset
  - Steps to fine-tune Seq-to-Seq models using datasets from Hugging Face.
  - File: [fine_tune_encoder_huggingface_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_seqtoseq_huggingface_dataset.ipynb)
  - Notes: dataset is larger, you may import the dataset your interested from the Hugging Face hub
- Fine Tune **Seq-to-Seq** Model for Keyword Extraction (Tutorial)
  - Steps to fine-tune Seq-to-Seq model to extract tech keywwords from texts. Follows the tutorial found [here.](https://medium.com/gitconnected/fine-tune-smaller-nlp-models-with-hugging-face-for-specific-use-cases-1745813471dc)
  - File: [fine_tune_seqtoseq_tech_keywords_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_seqtoseq_tech_keywords_dataset.ipynb)
  - Notes: we're using the dataset found [here](https://huggingface.co/datasets/ilsilfverskiold/tech-keywords-topics-summary). You may use another field rather than keywords, such as summary.

**Encoder** Models
- Fine Tune **Encoder for Classification** with Custom Dataset
  - Steps to fine-tune an encoder model for text classification using a custom dataset.
  - File: [fine_tune_encoder_classification_custom_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_encoder_classification_custom_dataset.ipynb)
  - Notes: you'll need to get ahold of your own dataset with text and label as fields

### Using
Instructions and examples for using models in an application.

- Pipeline Different Models
  - Demonstrates how to use different models using Hugging Face's pipeline in Colab.
  - File: [pipeline_testing_models.ipynb (Notebook)](./pipeline_testing_models.ipynb)
  - Notes: remember to find the models your keen to try on your own too in the Hugging Face Model [hub.](https://huggingface.co/models). 

### Create-Dataset
Creating a dataset can be tedious business. Use GPT-4 turbo to generate one for you that you can use to fine-tune. 

- [Script to generate additional fields with a CSV (repo)](https://github.com/ilsilfverskiold/gpt-create-dataset)

Here you will need a text it can transform in some way. The script above has a text field and is asking GPT-4 to generate keywords, summary and topic for each text. The script then iterates over the rows with the texts and creates a new csv file with the new fields that have been generated by GPT-4.
