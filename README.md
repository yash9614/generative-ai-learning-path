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
| 3 | `03-RAG-Systems` | Document Q&A, conversational RAG, **production RAG** (hybrid, rerank, eval) | 1–2 weeks |
| 4 | `04-Agents-and-LangGraph` | Tool calling, stateful agents, routing | 1–2 weeks |
| 5 | `05-Advanced-Projects` | Multi-agent (CrewAI), SQL chat, search engines | 1 week |
| 6 | `06-Fine-tuning-HuggingFace` | HF endpoints, fine-tuning Gemma | Optional |

---

## Must-Do Projects (Priority Order)

These give the highest learning ROI. Complete them in order.

1. **Stateful Chatbot with Memory** (`02-LangChain-Basics/chatbots-with-memory.ipynb`)
2. **LangGraph Tool-Calling Agent** (`04-Agents-and-LangGraph/langgraph-chatbot-with-tools.ipynb`)
3. **Conversational / Production RAG over Documents** (see `03-RAG-Systems/PRODUCTION-RAG-GUIDE.md`)
4. **LangGraph + Vector Store Routing**
5. **Chat with SQL**
6. **CrewAI Multi-Agent System**

---

## Key Concepts You Will Master

- LCEL for composable chains
- Message history and session management
- Embeddings, vector stores, and retrieval
- Hybrid search (dense + sparse) + Reciprocal Rank Fusion
- Cross-encoder reranking
- Query transformation and citations
- RAG evaluation (Hit@K + LLM-as-judge)
- Tool calling and function calling
- LangGraph state graphs, nodes, edges, and conditional routing
- Agent patterns (ReAct, routing, multi-agent)
- Prompt engineering for reliability

---

## Related Deep Notes

For concise, interview-focused concept notes (embeddings, RAG, MCP, LangGraph, CrewAI, Deep Agents, advanced RAG patterns, production FDE examples):

**[makan_m/learning-concepts](https://github.com/yash9614/makan_m/tree/main/learning-concepts)**

---

## Original Source

Materials curated and rearranged from the course dump at [zaap_corse](https://github.com/yash9614/zaap_corse).  
API keys have been removed and replaced with placeholders.

Happy learning! Start with `01-Foundations/README.md`.
