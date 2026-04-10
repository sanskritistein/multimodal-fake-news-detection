# Multimodal Fake News Detection

This project implements a multimodal fake news detection pipeline using textual and visual embeddings. The system compares a text-only baseline against multimodal early fusion and attention fusion, and also includes FAISS-based similarity retrieval.

## Project Overview

Fake news on social media often combines misleading text with persuasive visuals. This project studies whether multimodal learning can improve fake news detection compared with text-only methods.

## Methods

- Text encoder: BERT
- Image encoder: ResNet-50
- Baseline: Text-only classifier
- Multimodal model 1: Early fusion
- Multimodal model 2: Attention fusion
- Retrieval: FAISS nearest-neighbor search

## Dataset

The textual dataset was created from the Fake and Real News Dataset. A visual stream was attached to support multimodal experiments.

## Results

Three models were evaluated:

- Text-only baseline
- Early fusion
- Attention fusion

On the current experimental setup, the text-only model achieved the best F1-score, while the attention model learned to heavily prioritize text over image.

## Files

- `notebook/` - training and evaluation notebook
- `data/` - dataset file
- `models/` - trained model and retrieval artifacts
- `requirements.txt` - dependencies

## Future Work

- Use semantically aligned real news images
- Extend to video and social metadata
- Deploy a production web interface
