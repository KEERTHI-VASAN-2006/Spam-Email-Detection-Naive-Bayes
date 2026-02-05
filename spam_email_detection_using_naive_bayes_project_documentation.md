# Spam Email Detection using Naive Bayes

## 📌 Project Overview
Spam emails continue to be a major problem in digital communication, causing inconvenience, security risks, and productivity loss. This project implements a **Spam Email Detection System** using **Naive Bayes classification** to automatically classify emails as *Spam* or *Not Spam* based on their textual content.

The system applies **Natural Language Processing (NLP)** techniques and evaluates multiple Naive Bayes variants to determine the most suitable approach for text-based spam detection.

---

## 🎯 Objectives
- Apply **Naive Bayes** for text classification.
- Preprocess email text using **Bag of Words (BoW)** and **TF-IDF** feature extraction techniques.
- Implement **Multinomial Naive Bayes** and **Gaussian Naive Bayes**.
- Evaluate model performance using **Accuracy, Precision, Recall, and F1-score**.
- Demonstrate real-world usability using unseen email samples and visualizations.

---

## 🧠 Technologies & Libraries Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Google Colab

---

## 📂 Dataset
The dataset consists of labeled email messages with:
- `text`: Email content
- `spam`: Target label (0 = Not Spam, 1 = Spam)

---

## 🔄 Data Preprocessing Report

### 1. Data Cleaning
The following preprocessing steps were applied to email text:
- Conversion to lowercase
- Removal of numbers
- Removal of punctuation
- Removal of extra spaces
- Removal of empty email entries

### 2. Feature Extraction
Two feature extraction techniques were used:

#### Bag of Words (BoW)
- Implemented using `CountVectorizer`
- Converts text into word frequency vectors
- Suitable for Multinomial Naive Bayes

#### TF-IDF (Term Frequency–Inverse Document Frequency)
- Implemented using `TfidfVectorizer`
- Assigns weights based on word importance
- Reduces the influence of frequently occurring but less meaningful words

---

## 🤖 Model Implementation

### 1. Multinomial Naive Bayes
- Applied to both BoW and TF-IDF features
- Best suited for discrete text data

### 2. Gaussian Naive Bayes
- Applied to dense TF-IDF features
- Used for comparison purposes
- Less effective due to the continuous data assumption

---

## 📊 Performance Evaluation Report

### Evaluation Metrics Used
- Accuracy
- Precision
- Recall
- F1-score

### Results Summary

| Model | Feature Extraction | Performance |
|-----|------------------|------------|
| Multinomial NB | Bag of Words | Good |
| Multinomial NB | TF-IDF | **Best** |
| Gaussian NB | TF-IDF (Dense) | Lower |

### Observations
- TF-IDF with Multinomial Naive Bayes achieved the highest accuracy and F1-score.
- Gaussian Naive Bayes performed comparatively worse due to unsuitable data distribution assumptions.

---

## 📈 Visualizations
- Confusion Matrix for model evaluation
- ROC Curve with AUC score

These visualizations help analyze classification performance and model reliability.

---

## 🌍 Real-World Application
The trained model was tested on unseen email samples such as promotional messages and official communications. The classifier successfully identified spam and legitimate emails, demonstrating practical usability.

---

## ✅ Conclusion
This project successfully implements a spam email detection system using Naive Bayes classification. The results show that **Multinomial Naive Bayes with TF-IDF** is the most effective approach for text-based spam detection.

---

## 🚀 Future Enhancements
- Integration with a web or email client interface
- Use of advanced models like SVM or Deep Learning
- Real-time spam filtering system

---

## 👨‍💻 Author
**Keerthi Vasan S**

---

## 📎 How to Run
1. Open the notebook in Google Colab
2. Upload the dataset (`emails.csv`)
3. Run all cells sequentially
4. View results and visualizations

