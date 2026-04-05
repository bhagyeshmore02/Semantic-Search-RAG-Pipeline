# AI-Powered Semantic Search & RAG Pipeline for Product Reviews 🛒🤖

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Q6tGKkac1fXj_nGUlKhUe_xqVlDZRLO8?usp=sharing)

This project demonstrates how **Text Embeddings, Semantic Search, and Large Language Models (LLMs)** can be used to understand customer intent and retrieve meaningful product reviews, moving beyond the limitations of traditional exact-keyword matching.

The system uses **Sentence Transformers, FAISS vector search, and Google's Flan-T5 model** to find the most relevant reviews from a dataset of e-commerce product reviews and generate direct, human-like answers to user queries.

### 🚀 Project Overview

Traditional search systems rely on exact keyword matching, which often fails when a customer searches for "low power consumption" but the product is labeled "energy efficient." 

This project implements an **AI-powered Retrieval-Augmented Generation (RAG) pipeline** that understands the *meaning* of text using dense vector embeddings, retrieves relevant context, and uses an LLM to answer the customer's question directly.

**Example:**
* **User Query:** *"Does this consume a lot of electricity?"*
* **System Action:** Retrieves reviews related to battery life and power efficiency, even if the exact words are different, and generates a synthesized answer like: *"Based on customer reviews, this product is highly energy efficient and has low power consumption."*

### 🧠 Technologies Used

* Python
* Sentence Transformers (`all-MiniLM-L6-v2`)
* FAISS (Facebook AI Similarity Search)
* Hugging Face Transformers (`flan-t5-small`)
* Hugging Face Evaluate (ROUGE Metrics)
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-Learn (PCA)
* Google Colab

### 📊 Project Features

✔ Exploratory Data Analysis (EDA) of E-commerce text
✔ Text Embedding Generation using SBERT
✔ High-speed Semantic Search indexing using FAISS
✔ **Retrieval-Augmented Generation (RAG)** using a sequence-to-sequence LLM
✔ Automated AI Evaluation using ROUGE Metrics
✔ PCA Visualization of Semantic Embeddings

### 📂 Dataset & Source Code

* **Source Code:** [Click here to view and run the Google Colab Notebook](https://colab.research.google.com/drive/1Q6tGKkac1fXj_nGUlKhUe_xqVlDZRLO8?usp=sharing)
* **Dataset File:** `Dataset-SA.csv`
* **Data Fields Included:**
  * `product_name`: The specific name and model of the e-commerce item.
  * `product_price`: The retail price of the product.
  * `Rate`: The numeric customer rating (e.g., 1 to 5 stars).
  * `Review`: The short title or main keyword of the review (e.g., "awesome", "useless product").
  * `Summary`: The detailed customer feedback used to generate the dense semantic embeddings.
  * `Sentiment`: Pre-labeled sentiment classification (Positive, Negative, Neutral) used for data analysis.

### 🔎 How the Semantic Search & RAG Pipeline Works

1️⃣ Convert product review summaries into **vector embeddings** using Sentence Transformers.
2️⃣ Store and index these embeddings in a **FAISS vector index** for millisecond retrieval.
3️⃣ Convert the user's search query into a mathematical embedding.
4️⃣ Retrieve the most semantically similar reviews using vector similarity.
5️⃣ Pass the retrieved reviews as context to the **Flan-T5 Large Language Model**.
6️⃣ The LLM generates a direct, accurate answer to the user's query based *only* on the provided review context.

### 📈 Visualizations & Metrics Included

* **PCA Embedding Visualization:** A visual map proving that products with similar meanings naturally group together in vector space, regardless of vocabulary.
* **ROUGE Evaluation Scores:** Automated grading of the AI's generated answers against a ground-truth dataset to prove accuracy and reliability.

### 📌 Future Improvements

* Deploy the pipeline as an interactive web app using Streamlit
* Upgrade to a larger LLM for more complex reasoning 
* Build an automated product recommendation engine alongside the search
* Integrate a real-time data ingestion API for live reviews

### 👨‍💻 Author

**Bhagyesh More**
Student | AI & Software Development Enthusiast
Passionate about building practical AI-powered solutions, software tools, and seamless data pipelines. 

⭐ **If you found this project useful, feel free to star the repository! and contribute with me to build it better.**
