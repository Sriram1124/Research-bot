# Research Bot

A Retrieval-Augmented Generation (RAG) research assistant built using LangChain, FAISS, and HuggingFace embeddings. This bot analyzes news articles and answers research questions using semantic search and LLM-generated responses with source attribution.

---

## Overview

This project implements an end-to-end RAG pipeline that:

* Ingests news articles from URLs
* Splits articles into semantic chunks
* Converts text into vector embeddings
* Stores embeddings in a FAISS vector database
* Retrieves relevant context based on user queries
* Generates grounded answers using an LLM

---

## Architecture

```
News Articles
     ↓
Document Loader
     ↓
Text Splitter
     ↓
Embeddings Model
     ↓
FAISS Vector Index
     ↓
Retriever
     ↓
LLM
     ↓
Answer + Sources
```

---

## Tech Stack

* Python
* LangChain
* FAISS (Vector Database)
* HuggingFace Sentence Transformers
* Groq LLM
* Google Colab
* Jupyter Notebook

---

## Features

* Semantic search over articles
* Source-grounded answers
* Efficient vector similarity retrieval
* Automatic vector index creation and loading
* Fully reproducible notebook pipeline
* Modular and extensible architecture

---

## Project Structure

```
Equity-Research-Bot/
│
├── research_bot.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## How to Run

### Step 1: Open the notebook in Google Colab

Upload or open:

```
research_bot.ipynb
```

---

### Step 2: Install dependencies

Run the first cell in the notebook
---

### Step 3: Set your API key

set your api key defining the llm and i have used groq as it is cheaper and allows more requests
```

---

### Step 4: Run all notebook cells

The system will:

* Load and process articles
* Create the FAISS vector index (if not already created)
* Enable querying the research bot

---

## Example Usage

```python
query = "How many Cubans were deported during Trump's second term?"

response = chain.invoke({
    "question": query
})

print(response["answer"])
print(response["sources"])
```

---

## Example Output

```
Answer:
1,668 Cubans were deported during Trump's second term.

Source:
https://english.elpais.com/...
```

---

## Key Concepts Implemented

* Retrieval-Augmented Generation (RAG)
* Vector embeddings
* Semantic search
* Document chunking
* Vector databases (FAISS)
* Context-aware LLM responses

---

## Vector Index Handling

Vector index files are not included in the repository because they can be regenerated automatically from source documents.

This ensures portability and reproducibility.

---

## Use Cases

* Equity research automation
* Document analysis
* News intelligence systems
* Research assistants
* Knowledge retrieval systems

---

## Future Improvements

* Web interface deployment
* Cloud vector database integration
* Multi-source document ingestion
* Response ranking and reranking
* Real-time news ingestion

---

## Author

Developed as part of an applied Generative AI and Retrieval-Augmented Generation project.

---

