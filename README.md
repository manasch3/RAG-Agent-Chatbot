# RAG Agent Chatbot

A modern Retrieval-Augmented Generation (RAG) chatbot designed to answer questions from uploaded PDF documents using semantic search and AI-generated responses.

## Overview

This project combines document retrieval, vector embeddings, and large language model generation to provide context-aware answers grounded in your source documents. It is suitable for knowledge assistants, document Q&A systems, internal support tools, and AI-powered information retrieval workflows.

## Features

- Upload and process PDF documents
- Semantic retrieval using vector embeddings
- Context-aware question answering with LLM generation
- Responsive web interface
- Python + Flask backend with FAISS-based retrieval

## Tech Stack

- Python
- Flask
- Flask-CORS
- LangChain
- LangGraph
- FAISS
- Hugging Face Embeddings
- DeepSeek API
- PyPDF

## Project Structure

```text
rag-chatbot/
├── app.py
├── chat.py
├── requirements.txt
├── frontend/
│   ├── index.html
│   ├── script.js
│   └── styles.css
└── PDF/
```

## Prerequisites

- Python 3.10+
- A valid DeepSeek API key
- A valid Hugging Face API key (if required by your environment)

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/manasch3/RAG-Aagent-Chatbot.git
cd RAG-Aagent-Chatbot
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

Windows:

```bash
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and add the required keys:

```env
DEEPSEEK_API_KEY=your_deepseek_api_key_here
HUGGINGFACE_API_KEY=your_huggingface_api_key_here
```

### 5. Run the application

```bash
python app.py
```

Open the app in your browser at:

```text
http://localhost:5000
```

## How It Works

1. PDF files from the `PDF/` folder are loaded.
2. The content is split into smaller chunks.
3. Embeddings are generated using Hugging Face models.
4. FAISS stores the embeddings for similarity-based retrieval.
5. The LLM uses the retrieved context to generate accurate answers.

## License

This project is intended for educational, research, and demonstration purposes.

## Contact

For questions or collaboration opportunities, please use the repository discussion or contact channels associated with this project.
