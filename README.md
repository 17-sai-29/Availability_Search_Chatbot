# Availability_Search_Chatbot
This project implements a simple text-based chatbot that predicts the author of a given book title using a Naïve Bayes classifier built entirely

# 📚 Book Author Prediction using Naïve Bayes

This project is a simple NLP-powered chatbot that predicts the **author of a book** based on its title. The system uses a **Naïve Bayes classifier**..

---

## 🚀 Features

- 🔍 Predicts the **author** of a given book title.
- 🧠 Implements **Naïve Bayes classification from scratch**.
- 🗣️ Accepts **natural language queries** from the user.
- 🧾 Uses **POS tagging** to extract nouns from user input (via NLTK).
- 📊 Easily extensible to support book availability, books-by-author, etc.

---

## 📁 Dataset

The system uses a CSV file named `books3.csv` with the following columns:

| Book                | Author             | Availability |
|---------------------|--------------------|--------------|
| Wings of Fire       | A.P.J. Abdul Kalam | Available    |
| The Alchemist       | Paulo Coelho       | Unavailable  |
| ...                 | ...                | ...          |

Make sure `books3.csv` is placed in the same directory as the Python script.

---

## 🧠 How Naïve Bayes Works Here

1. **Training Phase**
   - Calculates prior probability of each author.
   - Computes likelihood of each word (from the book title) given the author.
   - Uses **Laplace smoothing** to handle unseen words.

2. **Prediction Phase**
   - Tokenizes the input book title.
   - Uses log-probabilities to avoid numerical underflow.
   - Applies Bayes' theorem to determine the most probable author.

---

## 🛠️ Requirements

- Python 3.x
- pandas
- nltk

Install dependencies:
```bash
pip install pandas nltk
