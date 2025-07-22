# 🚀 LogSense AI: Hybrid Log Classification Framework

## 📘 Overview

**LogSense AI** is a powerful, hybrid system for classifying log data using **three intelligent techniques**. Whether logs are predictable, complex, or unlabeled, this system is built to handle them all with precision.

It combines:
- 🔍 **Regex Matching** for simple patterns  
- 🧠 **ML with Sentence Transformers + Logistic Regression** for complex logs  
- 🤖 **LLM-based Classification** when labeled data is scarce

---

## 🔧 Classification Approaches

1. **🧾 Regular Expression (Regex)**
   - Ideal for clean and repetitive log patterns
   - Fast, rule-based classification

2. **📊 Sentence Transformer + Logistic Regression**
   - Converts log text into numerical embeddings
   - Applies a machine learning model to classify

3. **💡 LLMs (Large Language Models)**
   - Intelligent fallback for cases with limited training data
   - Works great with GPT-based models for open-ended pattern understanding

![architecture](resources/arch.png)

---

## 📁 Project Structure

| Folder/File | Purpose |
|-------------|---------|
| `training/` | Code for training regex and ML-based classifiers |
| `models/` | Stores trained Sentence Transformer embeddings and Logistic Regression models |
| `resources/` | Test data, outputs, architecture images, etc. |
| `server.py` | FastAPI server to host the classification API |

---

## ⚙️ Setup Instructions

### 1. Install Dependencies
Ensure Python is installed, then run:
```bash
pip install -r requirements.txt
