### **1. What is the difference between extractive and abstractive summarization?**

* **Extractive summarization** selects **existing sentences or phrases** from the original text that best represent its content.
* **Abstractive summarization** **generates new sentences**, rephrasing or paraphrasing ideas using natural language — like how humans summarize.

---

### **2. Why do methods based on TF-IDF/GraphRank select sentences rather than words?**

Because **meaning** is expressed in **sentences**, not individual words.

* TF-IDF or GraphRank compute importance scores for sentences to capture context and coherence.
* Isolated words lose the structure and logical flow of information.

---

### **3. What difficulties arise in the generation of abstractive summaries?**

* Maintaining **grammatical correctness**
* Preserving **factual accuracy**
* Avoiding **hallucinations** (invented facts)
* Ensuring **coherence and fluency**
* Handling **long input texts** due to limited model context length.

---

### **4. What are ROUGE metrics and how are they applied to assess quality?**

**ROUGE (Recall-Oriented Understudy for Gisting Evaluation)** compares model-generated summaries with reference summaries.

* Measures **overlap** of n-grams, words, and sequences.
* Common variants:

  * **ROUGE-1:** unigram (word) overlap
  * **ROUGE-2:** bigram overlap
  * **ROUGE-L:** longest common subsequence
    Used to evaluate how similar a generated summary is to human-written ones.

---

### **5. Why is grammatical correctness especially important for abstractive models?**

Because abstractive models **generate new sentences** — if grammar is wrong, the summary becomes unreadable or confusing, even if the facts are correct.
It directly affects **fluency and perceived quality**.

---

### **6. What is the difference between lexicon-based and ML-based approaches to sentiment analysis?**

* **Lexicon-based:** uses a predefined list of words with sentiment scores (e.g., *good = +1, bad = -1*).
* **ML-based:** trains a machine learning model on labeled data to learn sentiment patterns automatically (e.g., Naive Bayes, Logistic Regression, transformers).

---

### **7. Why is lemmatization needed?**

Lemmatization reduces words to their **base (dictionary) form** — e.g., *running → run, better → good.*
It helps:

* Reduce vocabulary size
* Improve matching between words with the same meaning
* Increase accuracy in text analysis and model training.

---

### **8. What does the confusion matrix show?**

It shows how many samples were **correctly or incorrectly classified** for each class.

* Rows = actual labels
* Columns = predicted labels
  Diagonal cells = correct predictions.

---

### **9. Why can accuracy sometimes be misleading?**

When the dataset is **imbalanced** (some classes much larger than others).
A model can get high accuracy by predicting only the majority class — while performing poorly on minority classes.
→ That’s why metrics like **precision, recall, F1-score** are also important.

---

### **10. What factors can interfere with the correct determination of sentiment?**

* **Sarcasm or irony** (e.g., *“Great, another delay.”*)
* **Negations** (*“not good”*)
* **Context ambiguity**
* **Domain-specific meaning** (*“killer feature”* is positive in tech, negative elsewhere).
* **Mixed sentiment** in the same sentence.

---

### **11. What is the difference between normalization and standardization of data?**

* **Normalization:** scales data to a fixed range (usually [0,1])
  → ( x' = \frac{x - x_{min}}{x_{max} - x_{min}} )
* **Standardization:** centers data around mean 0 and variance 1
  → ( x' = \frac{x - \mu}{\sigma} )

---

### **12. What is the advantage of TF-IDF over simple word frequency counts?**

TF-IDF considers both:

* **Term Frequency (TF):** how often a word appears in a document
* **Inverse Document Frequency (IDF):** how rare it is across all documents
  → So common words (“the”, “is”) get lower weight, and unique informative words get higher importance.

---

### **13. Why do abstractive models often make grammatical mistakes?**

Because they **generate text token-by-token**, predicting the next word probabilistically.
If training data is limited or model context is insufficient, it may lose grammatical consistency or agreement (tense, gender, etc.).

---

### **14. How does the ROC curve differ from the Precision-Recall curve?**

* **ROC curve:** plots **True Positive Rate (Recall)** vs **False Positive Rate**; best for balanced datasets.
* **Precision-Recall curve:** plots **Precision** vs **Recall**; more informative for **imbalanced datasets** (e.g., rare classes).

---

### **15. What is the Bag-of-Words method and how does it work?**

**Bag-of-Words (BoW)** represents a text as a collection of word counts, ignoring order and grammar.
Steps:

1. Create a **vocabulary** of all unique words.
2. Represent each document as a **vector of counts or frequencies**.
   Simple but effective for many NLP tasks like classification.
