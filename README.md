# 🧠 Tweet Sentiment Classification using Machine Learning

This project aims to **analyze sentiment in tweets** by classifying them as either **Good** or **Bad** sentiment. It uses natural language processing (NLP) techniques, multiple machine learning models, and provides a **graphical user interface (GUI)** using `Tkinter` to test predictions interactively.

---

## 📁 Project Structure

### ✅ Part A: Data Loading and Preprocessing

- Dataset: `twitter.csv`
- Columns: `id`, `label`, `tweet`
- Label Mapping:
  - `0 → Good sentiment detected`
  - `1 → Bad sentiment detected`
  - `2 → null`
- Special characters removed using regular expressions (`re.sub`).

---

### ✅ Part B: Model Training and Evaluation

- **Text Vectorization**: `CountVectorizer` used to convert tweets to numeric format.
- **Models Used**:
  - `DecisionTreeClassifier`
  - `RandomForestClassifier`
  - `LogisticRegression`

- **Performance Comparison**:
Decision Tree Accuracy: ~94.80%
Random Forest Accuracy: ~95.79%
Logistic Regression Accuracy: ~95.85%


- Accuracy is computed using `accuracy_score` from `sklearn`.

---

### ✅ Part C: GUI Application with Tkinter

- Developed a **Tkinter-based GUI** to:
- Select a tweet from a dropdown (`Combobox`).
- Predict its sentiment.
- Display result dynamically with:
  - Background color (Green = Good, Red = Bad, Gray = Unknown)
  - Result label (`ANALYSIS RESULT`)
- Clear the selection and reset UI.

- GUI includes:
- Combobox for tweet selection.
- "ANALYSE" button to predict.
- "Clear" button to reset.
- Dynamic UI updates based on prediction.

---

## 🧪 Sample Output

**Example 1**  
Input: `"factsguide society now motivation"`  
Prediction: `Good sentiment detected`

**Example 2**  
Input: `"oops carl paladino didnt mean to publicly post racist comments..."`  
Prediction: `Bad sentiment detected`

---

## ⚙️ Technologies Used

- Python 3.11
- Libraries:
- `pandas`
- `numpy`
- `nltk`
- `scikit-learn`
- `tkinter`

---

## ⚠️ Known Issues

- If `nltk` throws SSL errors during stopword download, you may need to add:
```python
import ssl
ssl._create_default_https_context = ssl._create_unverified_context
nltk.download('stopwords')


🚀 How to Run
Ensure all dependencies are installed.
Place twitter.csv in the same directory.
Run the notebook or the GUI script.
Use the GUI to test sentiment analysis on real tweets.
📌 Author
Subhash Kumar
MCA Final Semester | Android & Machine Learning Enthusiast


Would you like me to also help generate this as a downloadable `README.md` file or upload-ready zip with script and assets?
