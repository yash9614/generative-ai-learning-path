# Generative AI Learning Path

**A structured, beginner-to-advanced path covering LangChain, RAG, LangGraph Agents, Hugging Face, and practical projects.**

This repository rearranges high-value course materials into a clear learning journey. The original dump is left untouched. Focus on understanding concepts, running the notebooks, and completing the highlighted must-do projects.

---

## How to Use This Repo

1. Follow the numbered folders in order.
2. Read each section’s `README.md` before diving into notebooks.
3. Set up a virtual environment and install requirements as you go.
4. Use environment variables (`.env`) for all API keys — never hardcode them.
5. Complete the **Must-Do Projects** listed at the bottom and in `MUST-DO-PROJECTS.md`.

### Recommended Setup
```bash
python -m venv .venv
source .venv/bin/activate   # or .venv\Scripts\activate on Windows
pip install langchain langchain-groq langchain-community langgraph chromadb
# Add more packages as needed per notebook
```

Create a `.env` file:
```
GROQ_API_KEY=your_key_here
HUGGINGFACEHUB_API_TOKEN=your_token_here
LANGCHAIN_API_KEY=your_langsmith_key
```

---

## Learning Path Overview

| Stage | Folder | Focus | Time Estimate |
|-------|--------|-------|---------------|
| 1 | `01-Foundations` | NLP basics, embeddings, RNNs, transformers | 1–2 weeks |
| 2 | `02-LangChain-Basics` | Chains, prompts, memory, LCEL, chatbots | 1 week |
| 3 | `03-RAG-Systems` | Document Q&A, conversational RAG, hybrid search | 1–2 weeks |
| 4 | `04-Agents-and-LangGraph` | Tool calling, stateful agents, routing | 1–2 weeks |
| 5 | `05-Advanced-Projects` | Multi-agent (CrewAI), SQL chat, search engines | 1 week |
| 6 | `06-Fine-tuning-HuggingFace` | HF endpoints, fine-tuning Gemma | Optional |

---

## Must-Do Projects (Priority Order)

These give the highest learning ROI. Complete them in order.

1. **Stateful Chatbot with Memory** (`02-LangChain-Basics/chatbots-with-memory.ipynb`)  
   Learn message history, session IDs, prompt templates, and trimming.

2. **LangGraph Tool-Calling Agent** (`04-Agents-and-LangGraph/langgraph-chatbot-with-tools.ipynb`)  
   Build a ReAct-style agent with Wikipedia + Arxiv tools, conditional routing, and streaming.

3. **Conversational RAG over Documents**  
   Implement document loading → chunking → embedding → retrieval → generation with chat history.

4. **LangGraph + Vector Store Routing**  
   Route queries between a vector database and external search.

5. **Chat with SQL**  
   Natural language interface over a database.

6. **CrewAI Multi-Agent System**  
   Define agents, tasks, and tools that collaborate.

---

## Key Concepts You Will Master

- **LCEL** (LangChain Expression Language) for composable chains
- Message history and session management
- Embeddings, vector stores, and retrieval
- Hybrid search (dense + sparse)
- Tool calling and function calling
- LangGraph state graphs, nodes, edges, and conditional routing
- Agent patterns (ReAct, routing, multi-agent)
- Prompt engineering for reliability

---

## Original Source

Materials curated and rearranged from the course dump at [zaap_corse](https://github.com/yash9614/zaap_corse).  
API keys have been removed and replaced with placeholders.

Happy learning! Start with `01-Foundations/README.md`.
