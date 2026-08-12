
# Code-Switching Language Identification — CodeSaviours SI-26

## What This Repo Contains
- `SI-Week6-Fatima.ipynb` — Colab notebook for dataset labeling
- `SI-Week7-Fatima.ipynb` — Colab notebook for model training
- `dataset.csv` — Labeled dataset (word-level URD/ENG/MIX tags)

## Dataset
- 200 real code-switched sentences
- Collected from Twitter/X, Reddit (r/pakistan), YouTube comments, WhatsApp messages, and Facebook public pages
- 1357 total word entries, labeled as:
  - `URD` — Roman Urdu word
  - `ENG` — English word
  - `MIX` — word blending both languages

## Model
Fine-tuned `xlm-roberta-base` for token classification (language ID) on the dataset above.

- Training: 5 epochs, batch size 16
- Final validation loss: 0.208
- Framework: Hugging Face Transformers + PyTorch

**Model:** [huggingface.co/Fatimasajid/language-id-codesaviours-si26-fatima](https://huggingface.co/Fatimasajid/language-id-codesaviours-si26-fatima)

## Dataset Link
Hugging Face: https://huggingface.co/datasets/Fatimasajid/code-switching-codesaviours-si26-fatima

## Tools Used
Python, pandas, Google Colab, Hugging Face Transformers & Datasets, XLM-RoBERTa

## Author
Fatima Sajid — BS Computer Science, University of Faisalabad
Code Saviours SI-26 AI/ML Internship (ID: SI26-ML-FS-016)
