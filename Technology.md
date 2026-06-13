# Smart-Hire: AI & Machine Learning Pipeline

This directory contains the core Artificial Intelligence and Machine Learning codebase for the **Smart-Hire** platform. This component functions as a decoupled analytics microservice built in **Python**, responsible for raw text extraction, Natural Language Processing (NLP) entity extraction, and vector-based candidate ranking.

---

## 🛠️ AI/ML Tech Stack
* **Programming Language:** Python 3.x
* **NLP Framework:** Spacy (en_core_web_sm / custom NER pipelines)
* **ML Algorithms & Scoring:** Scikit-Learn (TF-IDF Vectorizer & Cosine Similarity)
* **Text Extraction Utilities:** PyPDF2 / PDFMiner / Docx2txt
* **Microservice API Gateway:** FastAPI / Flask

---

## 🧠 Algorithmic Workflow & Model Architecture

The core ML pipeline is divided into three consecutive processing stages:

### 1. NLP Entity Extraction (Named Entity Recognition)
* **Mechanism:** Ingests raw unstructured text data string compiled from PDF/DOCX resume file uploads.
* **Processing:** Uses **Spacy** pipelines coupled with custom regex pattern matchers to isolate specific text sequences.
* **Target Categories:** Extracts Key Skills arrays, computed Years of Experience metrics, and educational degrees.

### 2. Feature Vectorization (TF-IDF)
* **Mechanism:** Converts raw natural language text string entities into standardized mathematical matrices using **TF-IDF (Term Frequency-Inverse Document Frequency)**.
* **Processing:** Evaluates term weight frequencies across the candidate resume documents relative to the core constraints specified in the Job Description (JD).

### 3. Compliance Ranking (Cosine Similarity)
* **Mechanism:** Evaluates directional compliance match percentages ($0\%$ to $100\%$) between the target Job Description vector ($A$) and Candidate Resume vectors ($B$).
* **Formula Model:** $$\text{Similarity}(A, B) = \frac{A \cdot B}{\|A\| \|B\|}$$
* **Processing:** Computes the directional cosine angle between high-dimensional vector spaces. A score near $1.0$ ($100\%$) represents an exact match context. The system then outputs an ordered leaderboard matrix sorted by descending similarity scores.

---

## 🚀 Microservice Local Setup

To deploy the Python ML microservice engine locally, ensure you have **Python 3.9+** installed, then run the following setup commands inside this folder:

```bash
# 1. Install necessary core AI/ML libraries
pip install fastapi uvicorn spacy scikit-learn pypdf2 docx2txt

# 2. Download the Spacy English language model pipeline
python -m spacy download en_core_web_sm

# 3. Initialize and boot the FastAPI local microservice server
uvicorn main:app --reload --port 5000
