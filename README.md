# rag-vision-language-captioning

# Retrieval-Augmented Vision-Language Image Captioning System

## Overview

This project investigates the effectiveness of inference-time retrieval augmentation for image captioning using pretrained vision-language models. The goal is to evaluate whether contextual information retrieved from visually similar images can improve caption generation quality without requiring additional model training.

## Methodology

The proposed pipeline combines:

* **CLIP (ViT-B/32)** for image similarity retrieval
* **CLIPScore** for representative caption selection
* **InstructBLIP** for image caption generation

For a given query image, visually similar images are retrieved from the MS COCO dataset. Selected captions from retrieved images are incorporated into the prompt as contextual information before caption generation.

## Experimental Setup

### Dataset

* MS COCO 2017 Validation Set

### Retrieval Parameters

* Top-k retrieval: 1, 3, 5, 10
* Retrieval pool sizes: 500 and 2000 images

### Evaluation Metrics

* BLEU-4
* CIDEr
* CLIPScore
* SPICE

## Results

The study found that retrieval augmentation did not consistently improve caption quality in a zero-shot setting. While visually similar images could provide useful context, semantically misaligned retrieved captions often degraded performance.

Additional experiments using randomly selected captions demonstrated that contextual noise significantly impacts caption generation quality.

## Technologies Used

* Python
* Google Colab
* PyTorch
* HuggingFace Transformers
* CLIP
* InstructBLIP
* NumPy
* Pandas

## Repository Contents

* `*.ipynb` — Experimental notebooks
* `Capstone_Report.pdf` — Final project report

## Author

Satya Sujan Chinamilli | M.Eng. Artificial Intelligence | University of Cincinnati
