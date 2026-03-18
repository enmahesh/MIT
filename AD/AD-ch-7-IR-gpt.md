# Introduction to Information Retrieval and Web Search

These notes cover the chapter **Introduction to Information Retrieval and Web Search** for exam preparation.

---

# 1. Information Retrieval Concepts

## 1.1 Introduction

**Information Retrieval (IR)** is the process of finding relevant information from a large collection of documents based on a user query.

Examples of documents:

* Web pages
* Books
* Research papers
* Emails
* Multimedia files

Example search query:

```
machine learning tutorial
```

The system returns **ranked results** that best match the query.

### Objectives of IR

* Retrieve relevant documents
* Retrieve information quickly
* Rank documents according to relevance

---

## 1.2 Comparing Database Systems and IR Systems

| Feature        | Database System | Information Retrieval System |
| -------------- | --------------- | ---------------------------- |
| Data           | Structured      | Unstructured                 |
| Query Type     | Exact           | Approximate                  |
| Output         | Exact records   | Ranked documents             |
| Query Language | SQL             | Keywords                     |

Example database query:

```sql
SELECT * FROM students WHERE id = 10;
```

Example search query:

```
best programming books
```

Key Difference:

* Databases require **precise queries**
* IR systems support **approximate matching**

---

## 1.3 Modes of Interaction

### 1. Query-Based Interaction

User enters keywords to retrieve documents.

Example:

```
data science tutorial
```

### 2. Browsing

Users navigate through categories instead of searching directly.

Example:

* Digital libraries
* Online stores

### 3. Relevance Feedback

Users mark results as **relevant or irrelevant**.

The system improves future results.

### 4. Filtering

System continuously filters information according to user preferences.

Example:

* News feeds

### 5. Interactive Retrieval

Process:

```
Query → Results → Modify Query → Improved Results
```

---

## 1.4 Generic Information Retrieval Pipeline

Steps involved in retrieving information.

### Step 1: Document Collection

A large number of documents are collected.

Examples:

* Websites
* Articles
* PDFs

### Step 2: Text Processing

Includes:

* Tokenization
* Stopword removal
* Stemming

Example:

Sentence:

```
Information retrieval systems are useful
```

Tokens:

```
information
retrieval
systems
useful
```

---

### Step 3: Indexing

Documents are indexed using **inverted index**.

Example:

| Term      | Documents |
| --------- | --------- |
| data      | D1, D2    |
| mining    | D2        |
| algorithm | D3        |

---

### Step 4: Query Processing

Example query:

```
data mining
```

The system searches for documents containing these terms.

---

### Step 5: Ranking

Documents are ranked using scoring methods such as:

* TF-IDF
* Cosine similarity
* BM25

---

### Step 6: Result Presentation

Results are shown as:

* Ranked documents
* Snippets
* Highlighted keywords

---

# 2. Retrieval Models

Retrieval models determine how documents are matched with queries.

---

## 2.1 Boolean Model

Uses Boolean operators:

* AND
* OR
* NOT

Example:

```
machine AND learning
```

Advantages:

* Simple
* Precise filtering

Disadvantages:

* No ranking of results

---

## 2.2 Vector Space Model

Documents and queries are represented as vectors.

Similarity is calculated using **cosine similarity**.

```
Similarity(Q,D) = cosine(Q,D)
```

Advantages:

* Supports ranking
* Measures relevance

---

## 2.3 Probabilistic Model

Uses probability theory.

Goal:
Estimate the probability that a document is relevant.

Popular algorithm:

```
BM25
```

---

## 2.4 Semantic Model

Focuses on **meaning of words** instead of keywords.

Example:

Query:

```
car
```

Related results may include:

* automobile
* vehicle

---

# 3. Types of Queries in IR Systems

---

## 3.1 Keyword Queries

Simple keywords.

Example:

```
database tutorial
```

---

## 3.2 Boolean Queries

Example:

```
database AND indexing
```

---

## 3.3 Phrase Queries

Exact phrase search.

Example:

```
"machine learning algorithm"
```

---

## 3.4 Proximity Queries

Words must appear close together.

Example:

```
information NEAR retrieval
```

---

## 3.5 Wildcard Queries

Use symbols such as `*`.

Example:

```
comput*
```

Matches:

* computer
* computing
* computation

---

## 3.6 Natural Language Queries

Full question format.

Example:

```
What is information retrieval?
```

---

# 4. Text Preprocessing

Text preprocessing prepares documents for indexing.

---

## 4.1 Stopword Removal

Common words are removed.

Examples:

* the
* is
* and
* of

---

## 4.2 Stemming

Reduces words to root form.

| Word      | Stem   |
| --------- | ------ |
| computing | comput |
| computer  | comput |
| computed  | comput |

---

## 4.3 Using a Thesaurus

Used to find synonyms.

Example:

```
car → automobile
```

---

## 4.4 Handling Digits and Punctuation

Remove or normalize punctuation and numbers.

Example:

```
Data-driven → datadriven
```

---

## 4.5 Information Extraction

Extract structured information from text.

Examples:

* Names
* Dates
* Locations

---

# 5. Inverted Indexing

An **inverted index** maps terms to documents.

Example:

| Term   | Documents |
| ------ | --------- |
| IR     | D1, D3    |
| search | D1, D2    |
| data   | D2        |

Advantages:

* Fast search
* Efficient storage

---

# 6. Evaluation Measures of Search Relevance

---

## 6.1 Precision

Measures accuracy.

```
Precision = Relevant Retrieved / Total Retrieved
```

Example:

If 8 out of 10 retrieved documents are relevant:

```
Precision = 8/10 = 0.8
```

---

## 6.2 Recall

Measures completeness.

```
Recall = Relevant Retrieved / Total Relevant
```

---

## 6.3 F-Score

Combines precision and recall.

```
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

---

## 6.4 Precision-Recall Curve

Graph showing relationship between:

* Precision
* Recall

Higher curve indicates better system performance.

---

# 7. Web Search and Analysis

---

## 7.1 Web Structure Analysis

Analyzes links between pages.

Important algorithms:

* PageRank
* HITS Algorithm

---

## 7.2 Web Content Analysis

Analyzes content of web pages.

Includes:

* Keyword analysis
* Topic detection

---

## 7.3 Web Usage Analysis

Analyzes user behavior.

Examples:

* Click patterns
* Navigation paths
* Search history

Applications:

* Recommendation systems
* Personalized search

---

## 7.4 Practical Applications

Used in:

* Search engines
* E-commerce
* Online advertising
* Recommendation systems

---

# 8. Trends in Information Retrieval

---

## 8.1 Faceted Search

Users filter results using categories.

Examples:

* Price
* Brand
* Date

---

## 8.2 Social Search

Uses social network data to improve results.

---

## 8.3 Conversational Information Access

Users interact using conversational systems.

Example:

* Voice assistants

---

## 8.4 Probabilistic Topic Modeling

Discovers hidden topics in documents.

Example method:

```
Latent Dirichlet Allocation (LDA)
```

---

## 8.5 Question Answering Systems

Systems that provide **direct answers**.

Example query:

```
Who is the president of Nepal?
```

---

# Exam Questions and Answers

## Short Questions

### 1. What is Information Retrieval?

Information Retrieval is the process of finding relevant information from large document collections using a user query.

---

### 2. What is an inverted index?

An inverted index is a data structure that maps terms to the documents containing them.

---

### 3. Define precision.

Precision measures the accuracy of retrieved documents.

```
Precision = Relevant Retrieved / Total Retrieved
```

---

### 4. Define recall.

Recall measures how many relevant documents are retrieved.

```
Recall = Relevant Retrieved / Total Relevant
```

---

### 5. What is stemming?

Stemming is the process of reducing words to their root form.

Example:

```
computing → comput
```

---

# Long Questions

### 1. Explain the generic IR pipeline.

The IR pipeline consists of:

1. Document collection
2. Text preprocessing
3. Indexing
4. Query processing
5. Ranking
6. Result presentation

These steps allow efficient searching of large document collections.

---

### 2. Explain retrieval models in IR.

Major retrieval models include:

* Boolean Model
* Vector Space Model
* Probabilistic Model
* Semantic Model

These models determine how documents are matched with queries.

---

### 3. Explain evaluation measures of IR systems.

Evaluation measures include:

* Precision
* Recall
* F-score
* Precision-recall curve

These metrics measure search system performance.

---

# End of Notes
