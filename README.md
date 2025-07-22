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
````

### 2. Run the FastAPI Server

Start the API server using:

```bash
uvicorn server:app --reload
```

API Access Points:

* Main API: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
* Swagger Docs: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
* ReDoc: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 📤 Usage Guide

1. Upload a CSV file to the API containing logs with two columns:

   * `source`
   * `log_message`

2. The system will return a new CSV file containing:

   * `target_label` → the predicted category for each log message.

---

## 📛 Disclaimer

**Copyright ©**

* Codebasics Inc
* LearnerX Pvt Ltd

> This project is intended **only for educational purposes**. Commercial use without permission is prohibited.






