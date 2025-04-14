# HABER-X-AI-Based-News-Classification

#  HaberX – Turkish News Classification with BERT & ALBERT

HaberX is a Turkish NLP project that classifies news articles into predefined categories using transformer-based models. We focused on fine-tuning BERT and ALBERT to automatically identify the category of Turkish news content with high accuracy. A Gradio-based interface makes it easy to interact with the model.

---

# Project Overview

The goal of this project is to build a news classification model that can categorize Turkish news articles into 5 classes: Politics, Economy, Science & Technology, Sports, and Health. The TTC-3600 dataset was preprocessed and enhanced with SMOTE to handle class imbalance.

---

# Models & Techniques

- **BERT**: We used the `dbmdz/bert-base-turkish-uncased` model from Hugging Face for contextual embedding.
- **ALBERT**: A lightweight version of BERT optimized for low-resource settings.
- **SMOTE**: Applied to improve performance on minority classes.
- **TF-IDF Vectorization**: For baseline comparisons and additional feature engineering.

---

# Features

-  Preprocessing: Punctuation removal, lowercasing, tokenization  
-  Model training: Fine-tuned BERT & ALBERT using SimpleTransformers  
-  Model evaluation: Accuracy, Precision, Recall, F1-score  
-  Data augmentation: SMOTE to address class imbalance  
-  User interface: Built with **Gradio** for live model interaction  

---

# Dataset

- **Name:** TTC-3600 (restructured)  
- **Samples:** 1511 Turkish news articles  
- **Classes:** 5 (Politics, Economy, Science & Tech, Sports, Health)  
- **Structure:** CSV file with two columns: `category` and `text`  

---

# Results

| Model   | Accuracy |
|---------|----------|
| BERT    | **93.0%** |
| ALBERT  | 84.1% before SMOTE → **93% after SMOTE** |

SMOTE significantly improved class-wise performance for underrepresented categories.

---

# How to Run

1. Install dependencies:
   ```bash
   pip install simpletransformers gradio imbalanced-learn scikit-learn

# Tools & Libraries
**Python, Pandas, SimpleTransformers, Scikit-learn**

**Hugging Face Transformers**

**SMOTE (imbalanced-learn)**

**Gradio**


# Future Improvements
**Test with other transformer models like DistilBERT or RoBERTa**

**Deploy model on a web app or mobile API**

**Collect a larger and more diverse Turkish news dataset**

**Add title/author metadata for improved classification**
