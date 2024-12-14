# Climate Change Conversational Chatbot

### Overview

This project focuses on building a conversational chatbot trained on a dataset about climate change. The chatbot leverages the DialoGPT model to answer questions and engage in discussions about climate change. It incorporates fine-tuning techniques to customize the model for this specific domain.

### Dataset

The dataset was designed to build a chatbot that can provide meaningful discussions about climate change. Each entry contains:

- Source: URL or origin of the FAQ.
- faq: The question or answer related to climate change.
- text_type: A tag indicating whether the entry is a question (q) or an answer (a).

The dataset is structured sequentially, ensuring that each question is followed by its corresponding answer.

### Features

- Fine-Tuned DialoGPT: A pre-trained conversational model fine-tuned on a climate change FAQ dataset.
- Real-Time Interaction: Includes a chatbot interface for real-time interactions.
- BLEU Score Evaluation: Measures the quality of generated responses against reference answers using BLEU scores.
- Model Export: Saves the fine-tuned model and tokenizer for future deployment.

### Project Workflow

##### Dataset Preparation:
- Dataset is extracted and preprocessed, cleaning text and splitting it into questions and answers.

##### Training:
- Fine-tuning the DialoGPT model on the dataset.
- Padding and attention masking are applied to ensure effective model training.

##### Evaluation:
- Evaluates the chatbot's performance using BLEU scores.
##### Deployment:
- Saves the model and tokenizer in a reusable format.
- Exports the model as a Hugging Face pipeline for easy deployment.

### Results

- BLEU Score: 0.0050 (indicative of basic performance; requires further fine-tuning and dataset enrichment).
- The chatbot demonstrates basic conversational capabilities, responding meaningfully to some inputs but may require further improvement for broader use cases.

### Source

https://www.kaggle.com/datasets/ishgirwan/climate-change-faqs/data
