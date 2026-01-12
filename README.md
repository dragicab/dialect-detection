# Detection of Dialects in Macedonian Speech using Audio and Textual Representations

This repository contains the implementation and experimental setup for my bachelor thesis focused on the **automatic detection of Macedonian dialects** using **textual and audio data** combined with **machine learning and deep learning techniques**.

The goal of this work is to explore whether dialectal differences in Macedonian speech can be automatically recognized and classified, even under conditions of limited and imbalanced data.

---

## 📌 Thesis Overview

Macedonian language is characterized by a rich dialectal diversity, which represents an important part of the cultural and linguistic heritage. However, these dialects are poorly represented in modern digital technologies and language resources.

This thesis investigates:
- how dialectal characteristics can be captured from **text and speech**,
- how different **feature representations** affect performance,
- and how **classical machine learning models compare to transformer-based approaches** in low-resource settings.

---

## 🎯 Objectives

- Build a structured dataset of Macedonian dialects (text and audio)
- Develop models for **automatic dialect classification**
- Compare:
  - classical ML models vs transformer models
  - text-based vs audio-based approaches
- Analyze performance under **imbalanced data conditions**

---

## 🗂 Dataset Description

The dataset includes:
- **Textual data** (sentences and segments labeled by dialect)
- **Audio data** (speech recordings converted to a unified format)

### Dialects
- Based on the official Macedonian dialectological classification
- Covers **23 dialect groups** from the territory of North Macedonia

### Formats
- Text: JSONL (`{"text": "...", "dialect": "..."}`)
- Audio: WAV (16 kHz, mono) with metadata in JSONL format

---

## ⚙️ Methodology

### Text-based Approaches
- **TF-IDF + Logistic Regression**
  - Baseline classical ML approach
  - Interpretable and stable with limited data
- **Transformer model (Multilingual BERT)**
  - Contextual embeddings
  - Fine-tuned for dialect classification

### Audio-based Approaches
- **MFCC + Random Forest**
  - Classical speech processing pipeline
  - Robust to noise and small datasets
- **Wav2Vec2 (Transformer-based speech model)**
  - Learns directly from raw audio signals
  - Evaluated under limited-resource conditions

---

## 📊 Evaluation

Models are evaluated using:
- **Accuracy**
- **Macro-F1 score** (to account for class imbalance)

The dataset is split into:
- Training set
- Validation set
- Test set (completely held out)

---

## 📈 Results Summary

- Text-based models outperform audio-based models
- TF-IDF + Logistic Regression shows the most stable performance
- Transformer models demonstrate potential but require larger and more balanced datasets
- Audio-based dialect detection is feasible but more sensitive to data limitations

---

## 🧠 Key Findings

- Data quality and preprocessing have a greater impact than model complexity
- Classical models can outperform deep learning approaches in low-resource settings
- Macedonian dialect detection is a feasible and promising research direction

---

## 🚀 Future Work

- Expand and balance the dialect corpus
- Explore **multimodal models** combining text and audio
- Train transformer models specifically for Macedonian dialect data

---

## 📚 Technologies Used

- Python
- Scikit-learn
- Hugging Face Transformers
- PyTorch
- Librosa
- NumPy / Pandas

