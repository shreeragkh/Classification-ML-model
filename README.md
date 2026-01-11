# 📘 Math Question Topic Classification (Classical Machine Learning)

## 📌 Project Overview
This project implements a **classical machine learning pipeline** to classify high school mathematics questions into subtopics such as **Algebra, Calculus, Geometry, and Probability**.  
Each question is stored as an individual JSON file, and classification is performed using **text-based features** extracted from the question statements.

The goal of the project is to demonstrate the application of **traditional NLP and machine learning techniques** for multi-class text classification.

---

## 📂 Dataset Structure
The dataset is organized in a folder-based labeling format:

```text
MATH/
└── test/
    ├── algebra/
    ├── calculus/
    ├── geometry/
    └── probability/
```

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

### 2. Feature Extraction
To effectively represent mathematical text, a **hybrid TF-IDF feature representation** is used:

#### 🔹 Word-level TF-IDF
- Unigrams and bigrams
- Captures mathematical terminology and phrases  
  (e.g., *quadratic equation*, *limit of function*)

#### 🔹 Character-level TF-IDF
- Character n-grams (length 3 to 5)
- Captures symbolic patterns such as variables, operators, and short expressions  
  (e.g., *sin*, *cos*, *x^2*, *dx*)

Both feature types are combined using **FeatureUnion**, allowing the model to leverage both semantic and structural information.

### 3. Label Encoding
- Topic labels are converted into numerical form using **Label Encoding**

### 4. Train-Test Split
- The dataset is split into training and testing sets using an **80-20 split**
- Stratified sampling is used to maintain class distribution

### 5. Model Training
- A **Linear Support Vector Machine (Linear SVM)** classifier is trained on the TF-IDF features
- The model learns to associate question text patterns with math topics

---

## 📊 Evaluation
The model is evaluated on the test set using **accuracy** as the primary metric.

**Model Accuracy:** 77%

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
