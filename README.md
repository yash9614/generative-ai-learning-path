# Generative AI Learning Path

**A structured, beginner-to-advanced path covering LangChain, RAG, LangGraph Agents, Hugging Face, and practical projects.**

This repository rearranges high-value course materials into a clear learning journey. The original dump is left untouched. Focus on understanding concepts, running the notebooks, and completing the highlighted must-do projects.

**Telusko course coverage** (through Advance LangGraph Nov 2026) is reflected in the stage notes below and in the companion [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path) (see its `reference/TELUSKO-SESSION-MAP.md`).

---

## How to Use This Repo

1. Follow the numbered folders in order.
2. Read each section’s `README.md` before diving into notebooks.
3. Set up a virtual environment and install requirements as you go. Prefer `uv` (as used in the Telusko course).
4. Use environment variables (`.env`) for all API keys — never hardcode them.
5. Complete the **Must-Do Projects** listed at the bottom and in `MUST-DO-PROJECTS.md`.

### Recommended Setup
```bash
# Prefer uv
uv init
uv add langchain langchain-openai langgraph chromadb python-dotenv

# Or classic venv
python -m venv .venv
source .venv/bin/activate   # or .venv\Scripts\activate on Windows
pip install langchain langchain-openai langchain-community langgraph chromadb
```

Create a `.env` file:
```
OPENAI_API_KEY=sk-...
GROQ_API_KEY=your_key_here
HUGGINGFACEHUB_API_TOKEN=your_token_here
LANGCHAIN_API_KEY=your_langsmith_key
```

---

## Learning Path Overview

| Stage | Folder | Focus | Time Estimate |
|-------|--------|-------|---------------|
| 1 | `01-Foundations` | NLP basics, embeddings, RNNs, transformers | 1–2 weeks |
| 2 | `02-LangChain-Basics` | Chains, prompts, memory, LCEL, OpenAI SDK, Pydantic structured output | 1 week |
| 3 | `03-RAG-Systems` | Document Q&A, conversational RAG, **production RAG** (hybrid, rerank, eval) | 1–2 weeks |
| 4 | `04-Agents-and-LangGraph` | Tool calling, stateful agents, reducers, subgraphs, HITL, routing | 1–2 weeks |
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

- OpenAI API (chat + structured output) and LangChain wrappers
- LCEL for composable chains
- Message history and session management
- Embeddings, vector stores, and retrieval
- Hybrid search (dense + sparse) + Reciprocal Rank Fusion
- Cross-encoder reranking
- Query transformation and citations
- RAG evaluation (Hit@K + LLM-as-judge)
- Tool calling and function calling
- LangGraph state graphs, nodes, edges, reducers, subgraphs, Commands
- Human-in-the-loop interrupts and checkpointers
- Agent patterns (ReAct, routing, multi-agent)
- Prompt engineering for reliability

---

## Related Deep Notes

For concise, interview-focused concept notes and the full Telusko session map:

- **[makan_m/learning-concepts](https://github.com/yash9614/makan_m/tree/main/learning-concepts)**
- **[agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path)** (especially `reference/TELUSKO-SESSION-MAP.md`)

---

## Original Source

Materials curated and rearranged from the course dump at [zaap_corse](https://github.com/yash9614/zaap_corse).  
API keys have been removed and replaced with placeholders.

Happy learning! Start with `01-Foundations/README.md`.
