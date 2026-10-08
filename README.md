# 📰 Fake News Detection

> A Machine Learning and Natural Language Processing project for classifying news articles as **Fake** or **Real** based on their textual content.

---

## 📌 Overview

Fake news can spread rapidly through digital platforms, making automated detection an important Natural Language Processing (NLP) task.

This project builds a complete text classification pipeline that processes news articles, extracts meaningful textual features, and applies Machine Learning models to distinguish between fake and real news.

The project focuses on comparing different text representation techniques and classification models to evaluate their effectiveness.

---

## 🎯 Project Objectives

* Clean and preprocess raw news text
* Explore the structure and content of the dataset
* Transform text into numerical features
* Compare **Bag of Words (BoW)** and **TF-IDF**
* Train Machine Learning classification models
* Evaluate model performance using multiple metrics
* Identify an effective approach for fake news classification

---

## 📊 Dataset

The project combines two datasets:

* `Fake.csv` — Fake news articles
* `True.csv` — Real news articles

The datasets contain information such as:

| Feature   | Description           |
| --------- | --------------------- |
| `title`   | News article title    |
| `text`    | Full article text     |
| `subject` | News category/subject |
| `date`    | Publication date      |
| `label`   | Target class          |

The two datasets are combined into a single DataFrame, with:

* `0` → Fake News
* `1` → Real News

The combined dataset contains approximately **26.7K articles**.

---

## 🔄 Project Workflow

```text
Raw News Data
      ↓
Data Loading
      ↓
Label Assignment
      ↓
Data Combination
      ↓
Text Preprocessing
      ↓
Feature Extraction
   ↙          ↘
 BoW        TF-IDF
   ↓           ↓
Machine Learning Models
   ↓
Model Evaluation
   ↓
Fake / Real Classification
```

---

## 🧹 Text Preprocessing

The text preprocessing pipeline prepares the raw articles before converting them into machine-readable features.

The project uses **NLTK** for several NLP operations, including:

* Tokenization
* Stopword removal
* Text normalization
* Lemmatization
* Punctuation handling
* Text cleaning

The processed text is then used as the input for feature extraction.

---

## 🔢 Feature Extraction

Two different approaches are explored.

### 1. Bag of Words — BoW

The **CountVectorizer** technique represents each article based on the frequency of its words.

The project limits the vocabulary to the **3,000 most relevant features**.

### 2. TF-IDF

**TF-IDF (Term Frequency–Inverse Document Frequency)** represents words according to how important they are within the documents.

It also uses a maximum of **3,000 features**.

Both representations are evaluated using the same classification models to make the comparison more meaningful.

---

## 🤖 Machine Learning Models

### Logistic Regression

Logistic Regression is used as one of the main classification models.

It is evaluated using both:

* TF-IDF features
* Bag of Words features

### Multinomial Naive Bayes

Multinomial Naive Bayes is particularly suitable for text classification problems and is also evaluated with:

* TF-IDF
* Bag of Words

---

## 📈 Model Evaluation

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

For example, the Logistic Regression model using TF-IDF achieved approximately **98.57% accuracy** on the test set in the current notebook results.

The Naive Bayes model using Bag of Words achieved approximately **93.92% accuracy**.

> **Note:** These results are specific to the current dataset, preprocessing pipeline, and train/test split. They should not be interpreted as a guarantee of real-world fake-news detection accuracy.

---

## 🛠️ Technologies & Libraries

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## 📁 Repository Structure

```text
Fake_News/
│
├── Fake_News_Project.ipynb
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ahmed-ismail49/Fake_News.git
cd Fake_News
```

### 2. Install the required libraries

```bash
pip install pandas numpy nltk matplotlib seaborn scikit-learn
```

### 3. Add the datasets

Place the following files in the project directory:

```text
Fake.csv
True.csv
```

### 4. Run the notebook

Open:

```text
Fake_News_Project.ipynb
```

and run the cells sequentially.

---

## 💡 Key Takeaways

This project demonstrates an end-to-end NLP workflow:

**Data Preparation → Text Preprocessing → Feature Engineering → Model Training → Evaluation**

It also provides practical experience with comparing different text representations and Machine Learning algorithms for a real-world classification problem.

---

## 👤 Author

**Ahmed Ismail**

Data Science & Machine Learning

* GitHub: [ahmed-ismail49](https://github.com/ahmed-ismail49)
