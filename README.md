# Transformers-NLP-Docs

This repository is dedicated to providing documentation and practical guides for working with smaller open-source transformer models using the Hugging Face platform. It includes a range of resources from datasets and fine-tuning processes to business case applications for decoder, encoder and seq-to-seq transformer architectures.

## Contents

- [Docs](#docs)
  - [Models](#models)
- [Cook](#cook)
  - [Datasets](#datasets)
  - [Fine-Tune](#fine-tune)
  - [Using](#using)
  - [Creating Datasets](#create-dataset)

### Docs
Documentation on the different architectures, their base models, tasks and where it makes sense to fine-tune them. Also various examples of fine-tuned models from Hugging Face as examples.

#### Models
Detailed documentation on different transformer model architectures.
- [Decoder](./docs/models/decoder.md)
  - Business cases: [Decoder](./docs/business-cases/decoder.md)
- [Encoder](./docs/models/encoder.md)
  - Business cases: [Encoder](./docs/business-cases/encoder.md)
- [Seq-to-Seq](./docs/models/seq-to-seq.md)
  - Business cases: [Seq-to-Seq](./docs/business-cases/seq-to-seq.md)

### Cook
Cook books for fine-tuning, preprocessing datasets and using the models in an application.

#### Datasets
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

#### Fine-Tune
Cook books for the entire fine-tune process.
- Fine Tune Seq-to-Seq Model with Custom Dataset
  - Step by step script for fine-tuning Seq-to-Seq models using custom datasets.
  - File: [fine_tune_encoder_custom_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_seqtoseq_custom_dataset.ipynb)
  - Notes: dataset is smaller (8,500 rows) will be imported from Google Drive
- Fine Tune Seq-to-Seq with Hugging Face Dataset
  - Steps to fine-tune Seq-to-Seq models using datasets from Hugging Face.
  - File: [fine_tune_encoder_huggingface_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_seqtoseq_huggingface_dataset.ipynb)
  - Notes: dataset is larger, you may import the dataset your interested from the Hugging Face hub
- Fine Tune Encoder for Classification with Custom Dataset
  - Steps to fine-tune an encoder model for text classification using a custom dataset.
  - File: [fine_tune_encoder_classification_custom_dataset.ipynb (Notebook)](./cook/fine-tune/fine_tune_encoder_classification_custom_dataset.ipynb)
  - Notes: you'll need to get ahold of your own dataset with text and label as fields

#### Using
Instructions and examples for using models in an application.

- Pipeline Testing Models
  - Demonstrates how to use models using Hugging Face's pipeline in Colab.
  - File: [pipeline_testing_models.ipynb (Notebook)](./pipeline_testing_models.ipynb)
  - Notes: remember to find the models your keen to try on your own too in the Hugging Face Model [hub.](https://huggingface.co/models) 

#### Create-Dataset
Creating a dataset can be tedious business. Use GPT-4 turbo to generate one for you that you can use to fine-tune.

- [Script to generate additional fields with a CSV (repo)](https://github.com/ilsilfverskiold/gpt-create-dataset)
