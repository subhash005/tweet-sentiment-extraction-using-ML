# 🐦 Tweet Sentiment Analyzer (GUI + ML)

A machine learning-powered project that classifies the sentiment of tweets as **Good** or **Bad** — built with Python, scikit-learn, and an interactive Tkinter GUI.

---

## 📌 About the Project

This project analyzes real tweets and predicts their sentiment using traditional ML models. It also includes a desktop-based GUI app where users can select tweets from a dropdown and view the prediction with dynamic UI feedback.

No deep learning — just clean preprocessing, classic models, and practical implementation.

---

## 🗂 Dataset Overview

- File: `twitter.csv`
- Structure:
  - `id`: Tweet ID
  - `label`: Numeric category — `0` (Good), `1` (Bad), `2` (Null)
  - `tweet`: Text content of the tweet
  - `category`: Human-readable label mapped from `label`

---

## 🧹 Preprocessing Steps

- Removed special characters using `re` (regex)
- Removed stopwords using NLTK (`stopwords.words("english")`)
- Used `CountVectorizer` for feature extraction (BoW model)
- Converted all tweets to lowercase text vector representation

---

## 🤖 Models Trained

Using scikit-learn:
- ✅ Decision Tree
- ✅ Random Forest
- ✅ Logistic Regression

### 🔍 Accuracy Results:

| Model               | Accuracy   |
|--------------------|------------|
| Decision Tree       | 94.80%     |
| Random Forest       | 95.79%     |
| Logistic Regression | **95.85%** ✅ |

> ⚠️ Logistic Regression performed best on this dataset.

---

## 🧪 Test Example

```python
test_data = "oops carl paladino didnt mean to publicly post racist comments..."
prediction = clf.predict(cv.transform([test_data]))
# Output: 'Bad sentiment detected'
```
🖥️ GUI Application (Tkinter)
Simple and interactive GUI built using tkinter:
Select tweet from dropdown
Click ANALYSE to get result
Background color changes:
✅ Green: Good sentiment
❌ Red: Bad sentiment
⚪ Gray: Null or unclassified
Click Clear to reset the UI


🧰 Tech Stack
Python 3.x
Libraries:
pandas
numpy
scikit-learn
nltk
tkinter

🛠 Setup Instructions
pip install pandas numpy scikit-learn nltk

Then run:
import nltk
nltk.download('stopwords')

📁 Project Structure
tweet-sentiment-analyzer/
├── twitter.csv
├── tweet_classifier.ipynb     # Full analysis and training
├── app_gui.py (optional)      # If GUI is in separate script
└── README.md

🎓 Author
👤 Subhash Kumar
🧑‍🎓 MCA Final Year | Passionate about Android, Python & ML
📍 India


📌 Final Notes
This project focuses on practical implementation of NLP + ML with a simple GUI — no over-engineered models, just results that work.

