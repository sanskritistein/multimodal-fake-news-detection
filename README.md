# Multimodal Fake News Detection

This project presents a multimodal fake news detection framework using textual and visual embeddings. The system compares a text-only baseline with multimodal early fusion and attention fusion, and also includes FAISS-based similarity retrieval for related news search.

## Problem Statement

Fake news on social media is often presented through a combination of text and visuals. Text-only models can miss important multimodal cues, while multimodal systems must learn how to combine different sources of information effectively. This project investigates whether text-image fusion improves fake news classification and how retrieval can support analysis.

## Methods

- **Text Encoder:** BERT
- **Image Encoder:** ResNet-50
- **Baseline Model:** Text-only classifier
- **Multimodal Model 1:** Early fusion
- **Multimodal Model 2:** Attention fusion
- **Retrieval Module:** FAISS similarity search

## Dataset

The textual data was built from the Fake and Real News Dataset. Because this dataset does not include paired visual content, an image stream was attached to support multimodal experimentation.

## Results

Three models were evaluated:

- Text-only
- Early fusion
- Attention fusion

On the current setup, the text-only model achieved the best performance. The attention-fusion model assigned almost all importance to the textual modality, showing that the model correctly learned to down-weight the less informative visual modality.

## Repository Contents

- `Multimodal_Fake_News_Detection_Using_Text_and_Image_Embeddings_with_Attention_Fusion_and_Retrieval_Augmented_Analysis.ipynb` — main notebook
- `dataset.csv` — processed dataset
- `attention_fusion_model.pt` — trained attention model
- `faiss_index.bin` — FAISS retrieval index
- `train_meta.json` — metadata for retrieval results
- `results.csv` — evaluation results
- `requirements.txt` — required libraries

## Future Work

- Use semantically aligned real news images
- Extend to video and social-context features
- Deploy a full interactive interface
