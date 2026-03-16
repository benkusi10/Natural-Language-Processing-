# NLP Text Processing Exercises (Python)

## 📌 Overview

This project contains a set of **Python exercises focused on text preprocessing and pattern matching**, which are fundamental tasks in **Natural Language Processing (NLP)**.

The notebook demonstrates how to manipulate text data using:

* Python string methods
* Regular Expressions (`re` module)
* Basic text cleaning techniques used in NLP pipelines

These exercises help build foundational skills required for **text analysis, machine learning, and AI applications**.

---

# 📂 Project Structure

```
lab1_manipulate-text-data.ipynb
README.md
```

* **lab1_manipulate-text-data.ipynb** → Jupyter Notebook containing all exercises and solutions.

---

# 🧠 Topics Covered

## 1️⃣ Basic Text Manipulation

Using Python built-in string functions.

Tasks include:

* Converting text to lowercase
* Counting word occurrences
* Removing extra spaces
* Replacing keywords
* Filtering valid words

Example:

```python
sentence = "The Quick BROWN Fox Jumps Over The Lazy DOG"
result = sentence.lower()
```

---

## 2️⃣ Text Cleaning

Common preprocessing steps before training NLP models.

Examples:

* Removing extra whitespace
* Normalizing case
* Cleaning noisy text

Example function:

```python
def basic_clean(text):
    text = text.lower().strip()
    text = text.replace("\n", " ")
    text = " ".join(text.split())
    return text
```

---

## 3️⃣ Regular Expressions (Regex)

Using Python’s `re` module to extract patterns from text.

Exercises include:

* Extracting **years**
* Extracting **lowercase words**
* Finding **phone numbers**
* Identifying **prefix-based words**
* Extracting **dates**

Example:

```python
import re

text = "Python was created in 1991."
years = re.findall(r'\d{4}', text)
```

---

## 4️⃣ NLP Preprocessing Pipeline

Building a reusable function for cleaning raw text.

The function removes:

* URLs
* Emails
* Hashtags
* Mentions
* Punctuation
* Extra whitespace

Example:

```python
def preprocess_text(text):
    import re
    
    text = text.lower()
    text = re.sub(r'http\S+', '', text)
    text = re.sub(r'\S+@\S+', '', text)
    text = re.sub(r'[@#]\w+', '', text)
    text = re.sub(r'[^\w\s]', '', text)
    text = re.sub(r'\s+', ' ', text)
    
    return text.strip()
```

---

# 🚀 Skills Practiced

* Python string manipulation
* Regular expressions
* Text preprocessing
* NLP data cleaning
* Writing reusable functions

---

# 🛠 Technologies Used

* **Python 3**
* **Jupyter Notebook**
* Python **re (regex)** library

---

# 📚 Learning Goal

The goal of this exercise is to understand how **raw text data is cleaned and structured before being used in NLP models** such as:

* Sentiment Analysis
* Chatbots
* Text Classification
* Language Models

---

# 👨‍💻 Author

Created as part of a **Natural Language Processing practice lab** for learning text manipulation and regex in Python.
