# 🧠 NLP Basics with NLTK

This repository contains beginner-friendly implementations of core **Natural Language Processing (NLP)** techniques using the Python library **NLTK (Natural Language Toolkit)**.

It demonstrates how to preprocess text, analyze word frequency, perform stemming & lemmatization, remove stopwords, and extract named entities.

---

## 🚀 Features Covered

### 1. 🔤 Tokenization

Splitting text into words and sentences.

```python
from nltk.tokenize import word_tokenize, sent_tokenize
```

* `word_tokenize()` → splits text into words
* `sent_tokenize()` → splits text into sentences

---

### 2. 📊 Frequency Distribution

Counts how often each word appears in text.

```python
from nltk.probability import FreqDist

frequency = FreqDist()

for i in A:
    frequency[i] = frequency[i] + 1
```

#### Example Output:

```python
FreqDist({'NLP': 2, 'Hello': 1, 'and': 1, 'welcome': 1})
```

Useful methods:

```python
frequency.most_common(2)   # Top 2 frequent words
frequency['NLP']           # Frequency of specific word
```

---

### 3. ✂️ Stemming (Porter Stemmer)

Reduces words to their root form (may not be a real word).

```python
from nltk.stem import PorterStemmer

objporter = PorterStemmer()

objporter.stem('Making')   # make
objporter.stem('Welcome')  # welcome
```

---

### 4. 📖 Lemmatization (WordNet)

Returns the **actual base form** of a word.

```python
import nltk
nltk.download('wordnet')

from nltk.stem import WordNetLemmatizer

objlemmat = WordNetLemmatizer()

objlemmat.lemmatize('trouble')   # trouble
objlemmat.lemmatize('universe')  # universe
```

---

### 5. 🏷️ Part-of-Speech (POS) Tagging

Labels each word with its grammatical role.

```python
nltk.download('averaged_perceptron_tagger')

from nltk.tokenize import word_tokenize
from nltk.tag import pos_tag

text = "Harry lives in New York"
words = word_tokenize(text)
postags = pos_tag(words)
```

---

### 6. 🌍 Named Entity Recognition (NER)

Identifies real-world entities like **names, locations, organizations**.

```python
tree = nltk.ne_chunk(postags)
print(tree)

tree.draw()
```

📌 `ne_chunk()` groups words into entities such as:

* PERSON
* LOCATION
* ORGANIZATION

---

### 7. 🚫 Stopwords Removal

Removes common words that don’t add much meaning.

```python
from nltk.corpus import stopwords

stop_words = set(stopwords.words('english'))
```

#### Example:

```python
msg = "My name is shridhar mankar, I love making videos and watching kdrama."

words = word_tokenize(msg)

filtered_sentence = []

for w in words:
    if w not in stop_words:
        filtered_sentence.append(w)

print(words)
print(filtered_sentence)
```

---

## ⚙️ Installation

Install NLTK:

```bash
pip install nltk
```

Download required datasets:

```python
import nltk

nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')
```

---

## 📌 Summary

This project covers essential NLP preprocessing steps:

* Tokenization
* Frequency Analysis
* Stemming vs Lemmatization
* POS Tagging
* Named Entity Recognition
* Stopword Removal

These are foundational steps for building advanced NLP systems like:

* Chatbots 🤖
* Text classifiers 📊
* Search engines 🔍
* AI assistants

---

## 📁 Use Case

Perfect for:

* Beginners learning NLP
* Students working on AI/ML projects
* Anyone building text-processing pipelines

---

## ⭐ Contribute

Feel free to fork, improve, and expand this project with:

* More NLP techniques
* Visualization
* Machine Learning models

