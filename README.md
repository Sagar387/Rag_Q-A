# Rag_Q-A: Private Document Assistant

A retrieval-augmented generation (RAG) pipeline built with **LangChain**, **Pinecone**, and **OpenAI**. This project allows users to upload private PDF or DOCX documents, index them into a vector database, and perform semantic search to get context-aware answers.

## 🚀 Features
* **Multi-Format Support:** Load and process PDF and DOCX files.
* **Vector Search:** Utilizes Pinecone for high-performance similarity search.
* **Conversational Memory:** Maintains chat history for follow-up questions.
* **Custom Prompting:** Features a custom system prompt that can translate answers to French.

## 🛠️ Tech Stack
* **Framework:** LangChain
* **LLM:** OpenAI GPT-3.5 Turbo
* **Vector Database:** Pinecone (Serverless)
* **Local Vector Store:** ChromaDB
* **Embeddings:** OpenAI `text-embedding-3-small`

## 📋 Prerequisites
To run this notebook, you will need:
1.  An **OpenAI API Key**.
2.  A **Pinecone API Key**.
3.  Google Colab or a local Jupyter environment.

## ⚙️ Setup Instructions
1.  Clone the repository:
    ```bash
    git clone [https://github.com/Sagar387/Rag_Q-A.git](https://github.com/Sagar387/Rag_Q-A.git)
    ```
2.  Open the `Rag_QA.ipynb` in Google Colab.
3.  Add your API keys to the **Secrets** tab in Colab (key icon) as:
    * `OPENAI_API_KEY`
    * `PINECONE_API_KEY`
4.  Run all cells to initialize the pipeline.

## 📖 Usage
* **Loading:** Use `load_document(path)` to ingest your files.
* **Querying:** Use `ask_and_get_answer(vector_store, query)` for a single question.
* **Chatting:** Use the `ConversationalRetrievalChain` setup for a back-and-forth session with memory.
