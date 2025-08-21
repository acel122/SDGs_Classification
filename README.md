# Fine-tuning SDG Classifier  

This repository contains code for fine-tuning a **multi-label text classification model** to predict relevant **Sustainable Development Goals (SDGs)** from research abstracts or titles. The model is based on [sadickam/sdgBERT](https://huggingface.co/sadickam/sdgBERT) and trained using the Hugging Face Transformers library.  

## 📌 Features
- Preprocessing of text and SDG labels into multi-hot vectors.  
- Fine-tuning `sdgBERT` for **multi-label classification** (17 SDGs).  
- Metrics: F1 (micro), precision, recall, accuracy.  
- Hyperparameter tuning with **Ray Tune**.  
- Save & load trained model for inference.  
- Interactive CLI to test predictions on custom text input.  

---

## ⚙️ Installation

Clone this repo and install dependencies:

```bash
pip install transformers datasets scikit-learn evaluate ray[tune]
```

---
## 📂 Dataset

Note: The dataset used for training is private and not included in this repository.  
The expected format after preprocessing is an Excel file with at least these columns:  
- text: concatenation of title + abstract
- label: list of SDG labels, e.g. ['SDG 3', 'SDG 6']

During preprocessing, labels are converted to a multi-hot encoded vector for training.

---

## 📜 License

This project is for research purposes. Please check the license of [sadickam/sdgBERT](https://huggingface.co/sadickam/sdgBERT) before using it for commercial purposes.

