# 🤖 RAG Pipeline — LangChain + FAISS + OpenAI

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python) ![LangChain](https://img.shields.io/badge/LangChain-0.1+-1C3C3C) ![FAISS](https://img.shields.io/badge/FAISS-Meta-blue) ![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5/4-412991?logo=openai) ![License](https://img.shields.io/badge/License-MIT-green)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cre8vdj/cre8v-ai-rag/blob/main/rag_demo.ipynb)

A production-ready **Retrieval-Augmented Generation (RAG)** pipeline that enables you to **ask questions about your own documents** using LangChain, FAISS vector search, and OpenAI GPT. Upload PDFs, build a semantic index, and get accurate answers with citations.

---

## ✨ Features

- 📄 **PDF ingestion** — load and parse multiple PDF documents
- ✂️ **Text chunking** — smart splitting with overlap for context preservation
- 🧠 **Vector embeddings** — OpenAI `text-embedding-ada-002` for semantic search
- 🔍 **FAISS vector store** — fast approximate nearest-neighbor search
- 💬 **Conversational Q&A** — memory-aware multi-turn dialogue
- 📍 **Source citations** — each answer includes the source chunks
- 🔁 **Persistent index** — save and reload FAISS index to avoid re-embedding
- 🚀 **Google Colab ready** — run in the cloud with zero local setup

---

## 🎥 How It Works

```
PDFs → Text Chunks → Embeddings → FAISS Index
                                         ↓
              User Question → Similarity Search → Relevant Chunks
                                                        ↓
                                              GPT → Answer + Sources
```

---

## 🛠️ Tech Stack

| Library | Version | Purpose |
|---|---|---|
| LangChain | 0.1+ | RAG orchestration & chains |
| FAISS | 1.7+ | Vector similarity search |
| OpenAI | 1.x | Embeddings + GPT completion |
| PyPDF2 / pdfplumber | latest | PDF parsing |
| Python | 3.10+ | Language |

---

## 🚀 Getting Started

### Option 1: Google Colab (Recommended)

Click the badge above or visit:

> [Open in Colab](https://colab.research.google.com/github/cre8vdj/cre8v-ai-rag/blob/main/rag_demo.ipynb)

### Option 2: Run Locally

```bash
# Clone the repo
git clone https://github.com/cre8vdj/cre8v-ai-rag.git
cd cre8v-ai-rag

# Install dependencies
pip install langchain langchain-openai faiss-cpu pypdf openai python-dotenv

# Set your API key
export OPENAI_API_KEY="your-api-key-here"

# Launch Jupyter
jupyter notebook rag_demo.ipynb
```

---

## 📁 Project Structure

```
cre8v-ai-rag/
├── rag_demo.ipynb        # Main RAG notebook (end-to-end pipeline)
├── docs/
│   └── sample.pdf          # Example PDF for testing
├── requirements.txt      # Python dependencies
└── README.md
```

---

## 📎 Notebook Sections

| Section | Description |
|---------|-------------|
| 1. Setup | Install deps, configure API keys |
| 2. Load PDFs | Ingest and parse documents |
| 3. Chunking | Split text with RecursiveCharacterTextSplitter |
| 4. Embedding | Create vector embeddings with OpenAI |
| 5. FAISS Index | Build and save the vector store |
| 6. Q&A Chain | Setup ConversationalRetrievalChain |
| 7. Query | Ask questions and get cited answers |

---

## 🔑 Environment Variables

Create a `.env` file:

```env
OPENAI_API_KEY=sk-...
```

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

> Built by [cre8vdj](https://www.upwork.com/freelancers/~01fe4edd532e7be28f) · AI/ML Engineer · LLM & RAG Specialist
