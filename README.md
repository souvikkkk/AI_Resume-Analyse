# 🧠 AI Resume Analyzer using RoBERTa

A smart, AI-powered tool that analyzes resumes against job descriptions using **semantic similarity**, identifying matched skills, gaps, and offering improvement suggestions — just like a modern **ATS (Applicant Tracking System)**.

---

## 📌 Features

- ✅ Upload your resume and paste a job description to get a **match score**.
- 🔍 Identifies **matched and missing skills** using Named Entity Recognition (NER).
- 📊 Computes **semantic similarity** with RoBERTa instead of relying on exact keywords.
- 💡 Provides **personalized suggestions** for resume improvement.
- 🌐 Intuitive and clean web interface using Tailwind CSS.

---

## 💡 Why Semantic Matching?

Traditional resume checkers often fail to detect:

- **Synonyms** (e.g., “REST API” vs “Backend Service”)
- **Role equivalencies** (e.g., “Project Manager” vs “Product Owner”)
- **Skill clusters** and implicit responsibilities

By using **RoBERTa** (`stsb-roberta-large`), this analyzer evaluates the **meaning** of sentences instead of literal word matches.

---

## 🛠 Tech Stack

| Component            | Tech Used                         |
|----------------------|-----------------------------------|
| **Frontend**         | Tailwind CSS, HTML, Jinja2        |
| **Backend**          | Flask (Python)                    |
| **PDF Parsing**      | PyMuPDF                           |
| **Semantic Matching**| Sentence Transformers (`stsb-roberta-large`) |
| **Skill Extraction** | HuggingFace Transformers NER      |
| **Suggestions**      | Rule-based system                 |

---


---

## ⚙️ How It Works

1. **Upload Resume:** Accepts a `.pdf` resume.
2. **Paste Job Description:** Free-text input area for job requirements.
3. **Text Extraction:** Uses **PyMuPDF** to extract clean text from PDF.
4. **Semantic Scoring:**
   - Uses **RoBERTa** via `sentence-transformers` to compute semantic similarity.
   - Outputs a **match percentage score**.
5. **Skill Extraction:**
   - Uses NER pipeline to extract `SKILL`, `ORG`, `DEGREE`, etc.
   - Compares against job description keywords.
6. **Suggestion Engine:**
   - Highlights **missing skills**.
   - Provides **resume enhancement suggestions**.

---

## 📦 Installation

### Clone the Repo

git clone https://github.com/yourusername/ai-resume-analyzer.git    
cd ai-resume-analyzer

### Create the Virtual Enviroment

python -m venv venv    
source venv/bin/activate  # On Windows: venv\Scripts\activate

### Install Dependencies   

pip install -r requirements.txt

### Run the Flask App

python app.py


