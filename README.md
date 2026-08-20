
# Urdu OCR — Fine-Tuned TrOCR Model for Extracting Text from Urdu Images

Reads Urdu Nastaliq text from images and converts it into digital, editable text.

## Why This Matters

Urdu Nastaliq script is one of the hardest scripts for OCR tools to read — the letters connect and change shape depending on position, and most existing OCR tools (like Tesseract) fail on it completely. This project builds a working OCR pipeline specifically trained for Urdu, so documents, books, and images in Urdu can finally be searched, edited, and translated digitally instead of staying stuck as static images.

## Live Demo

Try it here: https://urdu-ocr-codesaviours-si26-fatima-few8uhqbwx8w99hug2o4rb.streamlit.app/

*(Deployed on Streamlit Community Cloud — Hugging Face Spaces free-tier limits blocked deployment there.)*

## How It Works

The model is a fine-tuned version of TrOCR (`Hammad712/troce-urdu-model2-v1`), trained on over 10,000 synthetic Urdu images generated using Noto fonts, plus manually labeled real images. Tesseract (a common open-source OCR engine) was tested first but read 0 out of 5 Urdu Nastaliq test images correctly, which is why a custom fine-tuned model was necessary. The final model takes an image as input and outputs the Urdu text found in it.

## Results

- Character Error Rate (CER): ~10.2%
- Trained over 10 epochs on 10,000+ synthetic images plus real labeled samples

## How to Run Locally

```bash
git clone https://github.com/fatimasajid31/urdu-ocr-codesaviours-si26-fatima.git
cd urdu-ocr-codesaviours-si26-fatima
pip install -r requirements.txt
streamlit run streamlit_app.py
```

## Built By

Fatima Sajid | Code Saviours SI-26 | 2026
