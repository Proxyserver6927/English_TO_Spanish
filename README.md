# English-to-Spanish Neural Machine Translation

A neural machine translation model using an encoder-decoder LSTM architecture built with Keras to translate English sentences into Spanish using the Tatoeba dataset.

# Project Structure

- `spa.txt` : Dataset containing English-Spanish sentence pairs  
- `English_to_Spanish.ipynb` : Jupyter Notebook with full code  
- `README.md` : Project documentation  

# Dataset

- **Source:** [Tatoeba](https://tatoeba.org/)  
- **Format:** Tab-separated values (TSV)  
- **Columns:**  
  - English sentence  
  - Spanish translation  
  - Metadata/comments  
- **Notes:** Used 124,596 pairs for training and 13,844 pairs for testing (total: 138,440 pairs)  

# Libraries Used

- pandas  
- numpy  
- matplotlib  
- re  
- string  
- scikit-learn  
- tensorflow  

**Note:** Keras is included in TensorFlow, so installing TensorFlow is sufficient.  

# Preprocessing Steps

- Convert text to lowercase  
- Remove punctuation and digits  
- Normalize whitespace  
- Add special tokens: `START_` and `_END` to Spanish sentences  

# Model Architecture

- **Type:** Encoder-Decoder  
- **Framework:** TensorFlow (Keras)  

## Encoder

- Embedding layer (dimension: 256)  
- Three stacked LSTM layers (each with 256 units)  

## Decoder

- Embedding layer (dimension: 256)  
- One LSTM layer (256 units)  
- Dense layer with softmax activation  

**Notes:**  
- Trained using teacher forcing  
- Uses padded sequences (max length: 70) and vocabulary indexing  

# Usage

## Setup

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow
