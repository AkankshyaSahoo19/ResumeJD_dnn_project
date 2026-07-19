# 📄 Resume-JD Match Scoring using Deep Neural Network

An AI-powered Resume Screening System that predicts how well a candidate's resume matches a job description using a **Deep Neural Network (Siamese BiLSTM Architecture)**. The project also highlights matching and missing skills to assist recruiters and job seekers.

## 📌 Project Overview

Recruiters spend significant time manually reviewing resumes against job descriptions. This project automates the process by learning semantic similarity between resumes and job descriptions using Deep Learning.

The system:

- Predicts whether a resume matches a job description.
- Provides a confidence score.
- Identifies matching skills.
- Identifies missing skills.

## 🎯 Objectives

- Automate resume screening.
- Reduce recruiter effort.
- Improve hiring efficiency.
- Provide explainable match results.

## 🛠 Technologies Used

- Python
- TensorFlow / Keras
- Bidirectional LSTM
- Siamese Neural Network
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

## 📂 Project Structure

```
ResumeJD_dnn_Project/
│
├── data/
│   ├── train.jsonl
│
├── screenshots/
│   ├── model accuracy.png
│   ├── model loss.png
│   └── confusion matrix.png
│
├── ResumeJD_dnn_Project.ipynb
└── README.md
```

## 📊 Dataset

The project uses Resume-Job Description matching datasets stored in **JSONL format**.

Each record contains:

- Resume Text
- Job Description
- Match Label

Example:

```
Resume:
Experienced Python developer with machine learning skills...

Job Description:
Looking for Python developer with NLP experience...

Label:
1 (Match)
```

## ⚙ Workflow

### 1. Data Loading

- Load JSONL dataset
- Convert into DataFrame

### 2. Data Preprocessing

- Lowercase conversion
- Remove punctuation
- Remove stopwords
- Tokenization
- Sequence padding

### 3. Feature Engineering

- Text vectorization
- Word embeddings
- Vocabulary creation

### 4. Model Architecture

The model uses a **Siamese Neural Network** consisting of:

- Shared Embedding Layer
- Shared BiLSTM Encoder
- Dense Layers
- Similarity Layer
- Sigmoid Output

Both resume and job description pass through identical encoders with shared weights.

## 🧠 Model Architecture

```
Resume
      │
Embedding
      │
BiLSTM
      │
Dense
      │
───────────────
               │
Similarity Layer
               │
Dense
               │
Sigmoid
               │
Match / No Match
               │
───────────────
Job Description
      │
Embedding
      │
BiLSTM
      │
Dense
```

---

## 📈 Model Evaluation

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Training Visualizations:

- Accuracy Curve
- Loss Curve

---

## 🔍 Prediction

Example Output

```
Resume-JD Match Result

Prediction : MATCH

Confidence : 94.83%

Matched Skills

✔ Python
✔ Machine Learning
✔ NLP
✔ SQL

Missing Skills

✘ Docker
✘ Kubernetes
✘ AWS
```

## 📷 Results

The trained model successfully learns semantic similarity between resumes and job descriptions and provides:

- Match Prediction
- Confidence Score
- Skill Comparison

making it suitable for intelligent resume screening.

## 📌 Future Improvements

- Transformer-based models (BERT, RoBERTa)
- Resume ranking system
- ATS compatibility score
- PDF Resume Parser
- Streamlit Web Application
- Multi-language support
