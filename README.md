# Transformers-NLP-Docs

This repository is dedicated to providing documentation and practical guides for working with smaller open-source transformer models using the Hugging Face platform. It includes a range of resources from datasets and fine-tuning processes to business case applications for various transformer architectures.

## Contents

- [Cook](#cook)
  - [Datasets](#datasets)
    - [Process Custom Dataset (file)](./cook/datasets/process_custom_dataset.ipynb)
    - [Process Hugging Face Dataset (file)](./cook/datasets/process_huggingface_dataset.ipynb)
    - [Push Custom Dataset to Hugging Face (file)](./cook/datasets/push_custom_dataset_huggingface.ipynb)
  - [Fine-Tune](#fine-tune)
    - [Fine Tune Encoder with Custom Dataset (file)](./cook/fine-tune/fine_tune_encoder_custom_dataset.ipynb)
    - [Fine Tune Encoder with Hugging Face Dataset (file)](./cook/fine-tune/fine_tune_encoder_huggingface_dataset.ipynb)
  - [Using](#using)
    - [Pipeline Testing Models](./pipeline_testing_models.ipynb)
- [Docs](#docs)
  - [Business Cases](#business-cases)
  - [Models](#models)

### Cook
Cook books for fine-tuning, preprocessing datasets and using the models in an application.

#### Datasets

##### Process Custom Dataset
[process_custom_dataset.ipynb](./cook/datasets/process_custom_dataset.ipynb) - Guide on how to process a custom dataset. 

**Notes:** this will be connecting to a csv file located in your Google Drive. We're importing it and then splitting it up to a training, testing and validation set.

##### Process Hugging Face Dataset
[process_huggingface_dataset.ipynb](./cook/datasets/process_huggingface_dataset.ipynb) - Steps to process datasets available on Hugging Face.

**Notes:** this will be importing a dataset located in Hugging Face, then setting a validation set from the training set (as it is missing), doing some slight filtering which is optional.

##### Push Custom Dataset to Hugging Face
[push_custom_dataset_huggingface.ipynb](./cook/datasets/push_custom_dataset_huggingface.ipynb) - Instructions on how to push a custom dataset to the Hugging Face hub.

**Notes:** this script imports a csv file from Google Drive, creates a dataset dict and then pushes it to the Hugging Face hub where you can share it with others (or keep it private).

#### Fine-Tune
Cook books for the entire fine-tune process.

##### Fine Tune Encoder with Custom Dataset
[fine_tune_encoder_custom_dataset.ipynb](./cook/fine-tune/fine_tune_encoder_custom_dataset.ipynb) - Tutorial for fine-tuning encoder models using custom datasets.

##### Fine Tune Encoder with Hugging Face Dataset
[fine_tune_encoder_huggingface_dataset.ipynb](./cook/fine-tune/fine_tune_encoder_huggingface_dataset.ipynb) - Steps to fine-tune encoder models using datasets from Hugging Face.

#### Using
Instructions and examples for using models in an application.

##### Pipeline Testing Models
[pipeline_testing_models.ipynb](./pipeline_testing_models.ipynb) - Demonstrates how to test models using Hugging Face's pipeline.

### Docs
Documentation on the different architectures, their base models, tasks and where it makes sense to fine-tune them. Also various examples of fine-tuned models from Hugging Face as examples.

#### Models
Detailed documentation on different transformer model architectures.
- [Decoder](./docs/models/decoder.md)
  - Business cases: [Decoder](./docs/business-cases/decoder.md)
- [Encoder](./docs/models/encoder.md)
  - [Encoder](./docs/business-cases/encoder.md)
- [Seq-to-Seq](./docs/models/seq-to-seq.md)
  - [Seq-to-Seq](./docs/business-cases/seq-to-seq.md)


