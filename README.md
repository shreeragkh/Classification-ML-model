# 📘 Math Question Topic Classification (Classical Machine Learning)

## 📌 Project Overview
This project implements a **classical machine learning pipeline** to classify high school mathematics questions into subtopics such as **Algebra, Calculus, Geometry, and Probability**.  
Each question is stored as an individual JSON file, and classification is performed using **text-based features** extracted from the question statements.

The goal of the project is to demonstrate the application of **traditional NLP and machine learning techniques** for multi-class text classification.

---

## 📂 Dataset Structure
The dataset is organized in a folder-based labeling format:

MATH/
└── test/
├── algebra/
├── calculus/
├── geometry/
└── probability/


- Each folder name represents a **topic label**
- Each JSON file contains a single math question
- Only the `problem` field is used for training to avoid data leakage

---

## 🧠 Problem Statement
Given a math question in textual form, the objective is to **predict its corresponding mathematical subtopic** using a classical machine learning model.

This is formulated as a **multi-class text classification problem**.

---

## 🔧 Methodology

### 1. Data Loading
- JSON files are read from each topic directory
- The folder name is used as the class label

### 2. Text Preprocessing & Feature Extraction
- Text data is converted into numerical features using **TF-IDF vectorization**
- Unigrams and bigrams are used to capture relevant mathematical terms
- Common English stop words are removed
- Vocabulary size is limited to 5000 features

### 3. Label Encoding
- Topic labels are converted into numerical form using **Label Encoding**

### 4. Train-Test Split
- The dataset is split into training and testing sets using an **80-20 split**
- Stratified sampling is used to maintain class distribution

### 5. Model Training
- A **Logistic Regression** classifier is trained on the TF-IDF features
- The model learns to associate question text patterns with math topics

---

## 📊 Evaluation
The model is evaluated on the test set using **accuracy** as the primary metric.

**Model Accuracy:** 69%

---

## 🛠 Technologies Used
- Python
- Scikit-learn
- TF-IDF Vectorizer
- Logistic Regression

---

## ✅ Conclusion
This project demonstrates that **classical machine learning approaches**, combined with effective text preprocessing, can successfully classify math questions into meaningful subtopics.  
The current implementation focuses on building and evaluating a reliable baseline model.

---

## 📌 Author
**Shreerag Namboothiri K H**
