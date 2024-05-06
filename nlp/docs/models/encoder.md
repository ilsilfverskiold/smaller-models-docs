# Encoder Models and Applications

Encoder models in natural language processing (NLP) are designed primarily to understand and encode information from text. These models are capable of processing and analyzing various forms of language data, transforming raw text into meaningful representations. They excel in tasks that require comprehension of context, such as text classification, named entity recognition, sentiment analysis, and more. 

Go [here](https://github.com/ilsilfverskiold/transformers-nlp-docs/blob/main/docs/business-cases/encoder.md) to get examples for different **business cases** for encoder models.

## Pre-training Objective
- **Fill-Mask**: Predicting masked words in a sentence.

## Base Models

### BERT (Bidirectional Encoder Representations from Transformers)
- **Overview**: A breakthrough model introducing bidirectional training for language models.
- **Released**: October 2018
- **Developed by**: Google AI.
- **Models in Hugging Face**: 
  - [BERT-base-uncased (110 M)](https://huggingface.co/bert-base-uncased)
  - [BERT-base-cased (109 M)](https://huggingface.co/bert-base-cased)

### ALBERT (A Lite BERT)
- **Overview**: Streamlined version of BERT, designed for similar performance with fewer parameters.
- **Released**: September 2019
- **Developed by**: Google Research and Toyota Technological Institute at Chicago.
- **Models in Hugging Face**:
  - [ALBERT-base-v2 (11.8 M)](https://huggingface.co/albert-base-v2)
  - [ALBERT-large-v2 (17.9 M)](https://huggingface.co/albert-large-v2)

### DistilBERT
- **Overview**: A distilled version of BERT, maintaining performance while being smaller and faster.
- **Released**: October 2019
- **Developed by**: Hugging Face.
- **Models in Hugging Face**:
  - [DistilBERT-base-uncased (67 M)](https://huggingface.co/distilbert-base-uncased)
  - [DistilBERT-base-multilingual-cased (135 M)](https://huggingface.co/distilbert-base-multilingual-cased)

### RoBERTa (Robustly Optimized BERT Approach)
- **Overview**: Builds upon BERT with modified hyperparameters and larger mini-batches.
- **Released**: July 2019
- **Developed by**: Facebook AI.
- **Models in Hugging Face**:
  - [RoBERTa-base (125 M)](https://huggingface.co/roberta-base)
  - [XLM-RoBERTa-base (279 M)](https://huggingface.co/xlm-roberta-base)

### ELECTRA (Efficiently Learning an Encoder that Classifies Token Replacements Accurately)
- **Overview**: Introduces a new pre-training approach focused on detecting replaced tokens.
- **Released**: March 2020
- **Developed by**: Stanford University and Google Research.

### DeBERTa (Decoding-enhanced BERT with Disentangled Attention)
- **Overview**: Improves BERT and RoBERTa with a novel disentangled attention mechanism.
- **Released**: June 2020
- **Developed by**: Microsoft.
- **Models in Hugging Face**:
  - [DeBERTa-base (139 M)](https://huggingface.co/microsoft/deberta-base)
  - [DeBERTa-large (304 M)](https://huggingface.co/microsoft/deberta-large)

## Tasks to Train For

### Text Classification
- **Examples**: Categorizing text into predefined categories.
  - [BERT-base-multilingual-uncased-sentiment](https://huggingface.co/nlptown/bert-base-multilingual-uncased-sentiment)
  - [Clinical-assertion-negation-bert](https://huggingface.co/bvanaken/clinical-assertion-negation-bert)
  - [Toxic-bert](https://huggingface.co/unitary/toxic-bert)

### Named Entity Recognition (NER)
- **Example**: Identifying and classifying named entities in text.
  - [BERT-base-NER](https://huggingface.co/dslim/bert-base-NER)

### Extractive Question Answering
- **Example**: Extracting answers from a text based on a query.
  - [BERT-large-uncased-whole-word-masking-finetuned-squad](https://huggingface.co/bert-large-uncased-whole-word-masking-finetuned-squad)

### Sentiment Analysis (Sub-task of Text Classification)
- **Examples**: Determining the sentiment expressed in text.
  - [Distilbert-base-multilingual-cased-sentiments-student](https://huggingface.co/lxyuan/distilbert-base-multilingual-cased-sentiments-student)
  - [Bert-base-go-emotion](https://huggingface.co/bhadresh-savani/bert-base-go-emotion)

### Part-of-Speech Tagging
- **Example**: Identifying grammatical parts of speech in text.

### Dependency Parsing
- **Example**: Analyzing the grammatical structure of a sentence.

### Semantic Role Labeling
- **Example**: Identifying the roles played by words in a sentence.

### Keyword Extraction
- **Example**: Identifying the main keywords or phrases in a text.
  - [Bert-uncased-keyword-extractor](https://huggingface.co/yanekyuk/bert-uncased-keyword-extractor)
  - [Bert-keyword-extractor](https://huggingface.co/yanekyuk/bert-keyword-extractor)

### Language Modeling
- **Example**: Predicting the likelihood of a sequence of words.

### Coreference Resolution
- **Example**: Identifying when different words refer to the same entity.

## Domain Specific Tasks

### Delicate Text Detection
- **Example**: Identifying and classifying text based on its level of delicateness or risk.
  - [Grammarly/detexd-roberta-base](https://huggingface.co/grammarly/detexd-roberta-base)

### ESG Text Mining
- **Example**: Extracting and processing information from texts related to Environmental, Social, and Governance (ESG) factors in sustainable investing.
  - [ESG-BERT](https://huggingface.co/nbroad/ESG-BERT)

 The list is not exhaustive. Please visit [Hugging Face Model Hub](https://huggingface.co/models) for more. 
