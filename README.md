MBTI Personality Analyzer (AI Project)
Predicting MBTI Personality Types Using Machine Learning & Voila Web App

Author: Aayush
Course: CSC-425

🔍 Project Overview

This project uses Artificial Intelligence to predict a person’s MBTI personality type based on their writing style.
The model analyzes text such as:

Social media posts

Quotes

Short essays

Paragraphs

User-typed messages

It determines the MBTI type (e.g., INTP, ESFJ, ENTJ) and provides a detailed explanation of each letter along with a one-sentence personality summary.

The final system is deployed as a web app using Voila and Binder, allowing anyone to interact with the project through a clean graphical interface—no code required.

🌐 Live Web App (Binder + Voila)

Click below to launch the MBTI Personality Analyzer:

Link: https://mybinder.org/v2/gh/aayus017/AI-MBTI-_app/HEAD?urlpath=voila/render/mbti_ai_project.ipynb

Note: Binder takes 1–3 minutes to load the first time.

🧠 How It Works
1. Dataset

The model is trained on the Kaggle MBTI 1.0 Dataset, which contains thousands of Reddit posts labeled with their MBTI type.
The notebook automatically downloads the dataset from HuggingFace.

2. Preprocessing

The text is cleaned by removing:

MBTI keywords (to avoid cheating)

URLs

Punctuation

Numbers

Extra spaces

Clean text is then transformed using TF-IDF vectorization.

3. Model Training

Instead of predicting all 16 MBTI types at once, the project trains four separate models, each for one MBTI dimension:

Dimension	Meaning
E / I	Extraversion vs Introversion
S / N	Sensing vs Intuition
T / F	Thinking vs Feeling
J / P	Judging vs Perceiving

All models use Logistic Regression, which performs well for text classification.

4. Prediction

The trained models are combined to generate a 4-letter MBTI type.
The app then displays:

The predicted MBTI type

One-sentence definition for each letter

A one-sentence summary of the overall type

5. User Interface

The interface is built with ipywidgets and includes two tabs:

Tab 1: MBTI From Text

Paste any text → The model predicts MBTI → Shows detailed explanation.

Tab 2: MBTI Quiz

A short interactive 4-question quiz → Estimates MBTI → Shows detailed explanation.
