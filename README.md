# Word2Vec & Semantic Similarity — NLP Assignment (Week 07 · Tuesday)

## 📌 Overview

This project implements **Word2Vec embeddings, polysemy analysis, disambiguation, and semantic similarity comparison** using movie overview text from TMDB.

It follows the assignment requirements:

* Word2Vec training
* Polysemy demonstration
* Context-based disambiguation
* Window size comparison
* Similarity comparison (BOW, TF-IDF, Word2Vec, Sentence-BERT)

---

## 📂 Dataset

Source: TMDB API (Top Rated Movies - Page 3)

```id="ds1"
https://api.themoviedb.org/3/movie/top_rated?api_key=8265bd1679663a7ea12ac168da84d2e8&language=en-US&page=3
```

Fields used:

* `overview` (text data)

---

## ⚙️ Installation

```id="inst1"
pip install pandas numpy requests gensim scikit-learn sentence-transformers
```

---

## ▶️ How to Run

1. Run the Python script:

```id="run1"
python tmdb_word2vec.py
```

2. Outputs include:

* Word similarity scores
* Disambiguation results
* Window size comparison
* Similarity scores (BOW, TF-IDF, Word2Vec, SBERT)

---

## 🧠 Implementation Details

### 1. Word2Vec Training

* Trained on cleaned movie overviews
* Parameters:

  * vector_size = 100
  * window = 5
  * min_count = 1

---

### 2. Polysemy (Q1a)

* Demonstrates that a word (e.g., "dark") has only **one embedding**
* Compared similarities with:

  * "evil"
  * "night"

---

### 3. Disambiguation System (Q1b)

* Uses:

  * Sentence embeddings (Word2Vec average)
  * Anchor vectors
* Predicts meaning based on cosine similarity

---

### 4. Window Size Comparison (Q1c)

* window = 2 → syntactic relations
* window = 10 → semantic relations

---

### 5. Similarity Comparison (Q2)

Compared:

* Bag of Words (BOW)
* TF-IDF
* Word2Vec averaging
* Sentence-BERT

---

## 📊 Key Observations

* BOW fails due to lack of semantic understanding
* TF-IDF improves slightly
* Word2Vec captures word-level meaning
* Sentence-BERT best captures sentence-level meaning

---

## 📁 Project Structure

```id="struct1"
week07/
 └── tuesday/
      ├── tmdb_word2vec.py
      ├── README.md
```

---

## ✅ Rubric Alignment

* ✔ All required tasks implemented
* ✔ Modular functions used
* ✔ Clean code (low hardcoding)
* ✔ Semantic explanations included
* ✔ Advanced model (SBERT) included

---

## 👨‍💻 Author

Vishal Pagadala

---

## 🚀 Notes

This project adapts the assignment dataset using TMDB movie overviews while preserving all required NLP concepts.
