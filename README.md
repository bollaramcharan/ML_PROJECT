🚀 Fake Job Detection System using NLP, Machine Learning & XGBoost

📌 Overview

The Fake Job Detection System is an end-to-end Machine Learning application that identifies fraudulent job postings using Natural Language Processing (NLP), Feature Engineering, and XGBoost Classification.

With the increasing number of online recruitment scams, this system helps job seekers verify whether a job posting is legitimate or potentially fraudulent by analyzing job descriptions, company details, requirements, and other recruitment information.

The solution combines:

NLP-based text analysis
Feature selection using Chi-Square statistics
XGBoost classification
Rule-based fraud intelligence
Interactive Streamlit dashboard
🎯 Problem Statement

Online job portals contain thousands of fake job advertisements that can lead to:

Financial scams
Identity theft
Data misuse
Wasted application efforts

The objective of this project is to build an intelligent fraud detection system capable of classifying job postings as:

✅ Legitimate Job

or

🚨 Fraudulent Job

with high accuracy and explainability.

🏗️ System Architecture
Job Posting Data
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Text Feature Engineering
(TF-IDF Vectorization)
        │
        ▼
Feature Selection
(Chi-Square)
        │
        ▼
XGBoost Classifier
        │
        ▼
Rule-Based Fraud Engine
        │
        ▼
Fraud Probability Score
        │
        ▼
Streamlit Dashboard
📂 Dataset
Fake Job Postings Dataset

The dataset consists of real-world recruitment advertisements containing both structured and unstructured information.

Dataset Statistics
Metric	Value
Total Records	17,880
Features	18
Target Variable	fraudulent
Real Jobs	Majority Class
Fake Jobs	Minority Class
Important Features
title
company_profile
description
requirements
employment_type
required_experience
required_education
industry
function
🔬 Machine Learning Pipeline
Step 1: Data Preprocessing
Missing value handling
Text cleaning
Feature consolidation
Null value replacement
Input normalization
Step 2: Feature Engineering

TF-IDF Vectorization was used to transform textual information into numerical feature vectors.

Features extracted from:

Job Title
Description
Requirements
Company Profile
Industry
Function
Step 3: Feature Selection

Chi-Square Feature Selection was applied to remove less important features and improve model efficiency.

Benefits:

Reduced dimensionality
Faster inference
Better generalization
Step 4: Model Training

Multiple algorithms were evaluated:

Model	Purpose
Logistic Regression	Baseline
Naive Bayes	NLP Benchmark
Random Forest	Ensemble Learning
XGBoost	Final Model
🏆 Final Model
XGBoost Classifier

Chosen due to:

Superior accuracy
Better handling of sparse TF-IDF features
Reduced overfitting
Faster prediction performance
Model Artifacts
model.pkl
tfidf.pkl
selector.pkl

These serialized objects are loaded directly into the Streamlit application for real-time inference.

🧠 Hybrid Fraud Detection Engine

Unlike traditional ML-only systems, this project implements a Hybrid Intelligence Layer.

Rule-Based Detection

Additional fraud indicators are generated when:

Company Profile is missing
Employment Type is missing
Industry is missing
Function is missing
Fraud Score Calculation
fraud_score += 1

When multiple critical fields are absent:

fraud_score >= 2

the system increases fraud confidence and flags the posting as suspicious.

Benefits
Improved robustness
Better handling of incomplete job postings
Reduced false negatives
Increased trustworthiness
💻 Web Application Features
🔍 Job Analysis Portal

Users can enter:

Job Title
Job Description
Requirements
Company Profile
Employment Type
Experience
Education
Industry
Function
🤖 AI Prediction Engine

The model automatically:

Cleans input
Generates TF-IDF features
Selects important features
Predicts fraud probability
Produces classification output
📊 Interactive Analytics Dashboard

The dashboard includes:

Fraud Probability Gauge

Visual indicators:

🟢 Low Risk (0-40%)

🟡 Medium Risk (40-70%)

🔴 High Risk (70-100%)

Performance Metrics
Model Accuracy
Dataset Size
Fraud Detection Count
AI Explanation Module

Provides reasoning behind predictions:

Missing information
Suspicious patterns
Poor quality descriptions
Incomplete employer details
🛠️ Technology Stack
Programming
Python 3.10
Machine Learning
Scikit-Learn
XGBoost
NLP
TF-IDF
NLTK
Data Processing
Pandas
NumPy
Visualization
Plotly
Matplotlib
Seaborn
Deployment
Streamlit
📁 Project Structure
Fake-Job-Detection-System/
│
├── app.py
├── ML_Final_Project.ipynb
├── fake_job_postings.csv
│
├── model.pkl
├── tfidf.pkl
├── selector.pkl
│
├── requirements.txt
├── README.md
│
└── screenshots/
🚀 Installation
Clone Repository
git clone https://github.com/yourusername/Fake-Job-Detection-System.git
cd Fake-Job-Detection-System
Create Environment
python -m venv venv
Activate Environment
venv\Scripts\activate
Install Dependencies
pip install -r requirements.txt
Run Application
streamlit run app.py
📈 Results
Model Performance
Metric	Score
Accuracy	95%
Precision	High
Recall	High
F1 Score	High
Key Achievements

✔ Detects fake jobs in real-time

✔ Uses NLP-based feature extraction

✔ Hybrid fraud intelligence layer

✔ Interactive dashboard visualization

✔ Production-ready deployment

🔮 Future Enhancements
Deep Learning Integration
LSTM
Bi-LSTM
Transformer Models
Generative AI
BERT-based Fraud Detection
RoBERTa Fine-Tuning
Explainable AI using SHAP
Deployment Improvements
Docker Containerization
AWS Deployment
REST API Development
Additional Features
Resume-to-Job Matching
Real-Time Job Scraping
Automated Fraud Alerts
Recruiter Verification System
👨‍💻 Author
Charan Bollaram

AI/ML Engineer | NLP Enthusiast | Generative AI Developer

📧 Email: your-email@example.com

🔗 LinkedIn: Add Your LinkedIn URL

💻 GitHub: Add Your GitHub URL
