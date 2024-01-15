# Recommender_hyper_personalisation
Outfit Recommendation with Text To Text Transfer Transformer ( T5) model

## Overview
This repository implements an outfit recommendation system using T5, focusing on understanding consumer behavior. The hypothetical dataset consists of past purchases ('Input') and the next item bought ('Output'), enabling the model to learn purchasing patterns and make relevant recommendations.

## Key Components:

1. T5 Model and Tokenization:
Utilizes the T5 model, a transformer-based architecture for sequence-to-sequence tasks. Tokenization is done using the AutoTokenizer from Hugging Face.

2. Prompt Creation:
Constructs a prompt for the T5 model by combining purchased and unpurchased items. This prompt provides context for the model to understand user history and suggest relevant items.

3. Training Data Preparation:
Splits data into training and evaluation sets, tokenizes them using the Hugging Face datasets library, and prepares them for model training.

4. Model Training:
Fine-tunes the T5 model using the Seq2SeqTrainer. Adjusts hyperparameters to enhance the model's understanding of purchasing patterns.

5. Inference:
Uses the trained model for inference on new input sequences, generating recommendations for the next item to purchase.

6. Evaluation:
Utilizes ROUGE metrics to evaluate recommendation quality by comparing model-generated recommendations to reference items.

A ROUGE score of 79 indicates a substantial overlap between the model-generated recommendations and the reference recommendations in terms of n-grams. In the context of outfit recommendations, this means that the model's suggestions closely match the user's actual purchases.

7. Results:
The recommended_dataframe contains final recommendations, including input prompts, target items, and model-generated suggestions.

## Prompt Justification:
The prompt creation step is crucial to guide the model in understanding the input context. By explicitly stating purchased items and candidates for recommendation, the model gains a clear understanding of user history, improving the relevance of generated recommendations.
