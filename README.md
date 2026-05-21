# RAG-Project- 
I developed a RAG-based research paper assistant using my own research papers as the knowledge source. The system allows users to ask questions in natural language, and the LLM generates answers using retrieved context from the papers.

# Agentic RAG System using LangGraph

This project is a complete implementation of Traditional RAG and Agentic RAG using LangGraph, LangChain, Gemini, and FAISS.

I built this project to understand how modern AI systems retrieve information from vector databases and generate intelligent responses using Large Language Models (LLMs).

The system can:
- retrieve information from stored documents
- generate answers using Gemini
- decide dynamically whether retrieval is required
- work as a simple AI agent using LangGraph

---

# Technologies Used

- Python
- LangChain
- LangGraph
- Gemini 2.5 Flash
- FAISS Vector Database
- HuggingFace Embeddings
- Streamlit
- uv Package Manager

---

# Embedding Model

```python
sentence-transformers/all-MiniLM-L6-v2
```

Used for generating semantic embeddings and similarity search.

---

# LLM Used

```python
gemini-2.5-flash
```

Used for:
- answer generation
- reasoning
- context understanding

---

# What I Implemented

## 1. Traditional RAG

Basic RAG pipeline:
- user query
- retrieve relevant documents
- generate answer using context

Flow:

```text
User Query
   ↓
Retriever
   ↓
Relevant Documents
   ↓
LLM
   ↓
Answer
```

---

## 2. Enhanced RAG

Added:
- confidence score
- source tracking
- better prompt handling
- improved retrieval logic

---

## 3. Advanced RAG

Added:
- streaming responses
- citations
- summarization
- history management

---

## 4. Agentic RAG using LangGraph

Implemented a decision-making workflow where the system first decides whether retrieval is needed.

If the query is related to stored data:
- retrieve documents from vector database

Otherwise:
- directly answer using the LLM

Flow:

```text
START
   ↓
Decision Node
   ↓
Need Retrieval?
   ↓
 ┌─────────────┐
 │             │
Yes           No
 │             │
 ↓             ↓
Retrieve    Direct Answer
 │
 ↓
Generate Answer
 │
 ↓
END
```

---

# Vector Database

FAISS is used as the vector database for:
- storing embeddings
- semantic similarity search
- document retrieval

---

# Sample Knowledge Base

The vector database currently stores information related to:
- LangGraph
- RAG
- Vector Databases
- Agentic AI Systems

---

# Streamlit Interface

A Streamlit chatbot UI was also created for interactive question answering.

Run using:

```bash
streamlit run app.py
```

---

# Installation

Clone repository:

```bash
git clone <your-repository-url>
cd <project-folder>
```

Initialize uv project:

```bash
uv init
```

Create virtual environment:

```bash
uv venv
```

Activate environment:

Windows

```bash
.venv\Scripts\activate
```

Linux/Mac

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
uv add langchain
uv add langgraph
uv add streamlit
uv add faiss-cpu
uv add sentence-transformers
uv add langchain-community
uv add langchain-google-genai
uv add python-dotenv
```

---

# Environment Variables

Create a `.env` file:

```env
GOOGLE_API_KEY=your_google_api_key
GROQ_API_KEY=your_groq_api_key
```

---

# Run Project

```bash
streamlit run app.py
```

---

# What I Learned

Through this project, I learned:
- Retrieval-Augmented Generation (RAG)
- Agentic RAG
- LangGraph workflows
- Embeddings and semantic search
- Vector databases
- LLM integration
- Streamlit application development
- AI agent workflows

---

# Future Improvements

- Multi-PDF support
- Conversational memory
- Hybrid search
- Multi-agent systems
- Web search integration
- Tool calling agents

---

# Author

Shubham Saurav

AI/ML Engineer | Generative AI Enthusiast

