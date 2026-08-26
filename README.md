
# Code-Switching Language Identification — Roman Urdu / English / MIX

Identifies which language each word belongs to in mixed Roman Urdu-English sentences — a common way people actually text and write online in Pakistan.

## Why This Matters

Most real-world text in Pakistan naturally switches between Roman Urdu and English within the same sentence (for example: "yaar mujhe ye assignment submit karna hai by tonight"). Standard NLP tools struggle with this kind of mixed text because they're built for one language at a time. This project labels each word as Urdu (URD), English (ENG), or Mixed (MIX), which is a foundational step for building better chatbots, translators, and text analysis tools for South Asian languages.

## Live Demo / Model

Model on Hugging Face: https://huggingface.co/Fatimasajid/language-id-codesaviours-si26-fatima
https://huggingface.co/spaces/Fatimasajid/code-switching-demo

## How It Works

A 200-sentence Roman Urdu-English code-switching dataset was created with word-level URD/ENG/MIX labels. An XLM-RoBERTa model was then fine-tuned on this dataset for token classification — meaning it looks at each word individually in a sentence and predicts which language it belongs to, rather than judging the sentence as a whole.

## Results

Strong F1 scores were achieved across all three label categories (URD, ENG, MIX) after fine-tuning.

## How to Run Locally

```bash
git clone https://github.com/fatimasajid31/code-switching-codesaviours-si26-fatima.git
cd code-switching-codesaviours-si26-fatima
pip install transformers torch
```

```python
from transformers import AutoTokenizer, AutoModelForTokenClassification

tokenizer = AutoTokenizer.from_pretrained("Fatimasajid/language-id-codesaviours-si26-fatima")
model = AutoModelForTokenClassification.from_pretrained("Fatimasajid/language-id-codesaviours-si26-fatima")
```

## Built By

Fatima Sajid | Code Saviours SI-26 | 2026
