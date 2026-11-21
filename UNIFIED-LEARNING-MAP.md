# 🚀 Generative AI Unified Learning Map

> **Cross-resource compass** for this Generative AI Learning Path.  
> Synthesizes high-signal materials from sunnysavita10, CampusX (campusx-official + Yash-Kavaiya/CampusX-courses), Telusko, and complementary tutorials so you can jump straight to the right notebook or folder.

**Use this alongside the stage folders in this repo.** Pair it with [MUST-DO-PROJECTS.md](MUST-DO-PROJECTS.md) and the companion [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path).

---

## 🎯 Core Overlap — What the Best GenAI Resources Emphasize

| Priority | Concept | Why It Matters | Best Coverage (Direct Links) |
|----------|---------|----------------|------------------------------|
| ⭐⭐⭐⭐⭐ | **Foundations (Embeddings, Transformers)** | Solid base before tools | sunnysavita10 Full-Stack Bootcamp Classes 1–15 · [Generative-AI-Indepth-Basic-to-Advance](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) · Stage 01 |
| ⭐⭐⭐⭐⭐ | **LangChain Basics + LCEL** | Composable chains & prompts | [campusx-official/langchain-models](https://github.com/campusx-official/langchain-models) · [langchain-prompts](https://github.com/campusx-official/langchain-prompts) · Stage 02 |
| ⭐⭐⭐⭐⭐ | **RAG (Basic → Production)** | Document Q&A that works in practice | [sunnysavita10/Generative-AI-Indepth-Basic-to-Advance](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) · [Full-Stack Bootcamp RAG classes](https://github.com/sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0) · Stage 03 + PRODUCTION-RAG-GUIDE |
| ⭐⭐⭐⭐ | **LangGraph Agents & Workflows** | Stateful, tool-using systems | [campusx-official/langgraph-tutorials](https://github.com/campusx-official/langgraph-tutorials) · [chatbot-in-langgraph](https://github.com/campusx-official/chatbot-in-langgraph) · Stage 04 |
| ⭐⭐⭐⭐ | **Tool Calling + Memory** | Agents that act and remember | Stage 04 notebooks · CampusX LangGraph tools/persistence |
| ⭐⭐⭐ | **Multi-Agent (CrewAI / Orchestrator)** | Specialized collaboration | Stage 05 · sunnysavita later classes |
| ⭐⭐⭐ | **Fine-tuning & Hugging Face** | Custom models | Stage 06 · sunnysavita fine-tuning classes (18–28) |
| ⭐⭐⭐ | **Evaluation** | Know if it actually works | sunnysavita Classes 58–59 (DeepEval) · RAG evaluation patterns |

---

## 📚 Resource Map

### Primary External Sources

| Resource | Style | Strengths | How to Use With This Path |
|----------|-------|-----------|---------------------------|
| [sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0](https://github.com/sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0) | 59-class full-stack bootcamp (Mar–Nov 2026) | Deep foundations → fine-tuning → RAG → agents → MCP → evaluation. Interview Q bank + DeepEval | Classes 1–16 → Stage 01; 29–39 → Stage 03; 40–52 → Stage 04; 53–59 → advanced |
| [sunnysavita10/Generative-AI-Indepth-Basic-to-Advance](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) | Practical notebooks (541★) | Hybrid search, reranking from scratch, multimodal RAG, memory, multi-doc chat | Excellent complement to Stage 03 production RAG |
| [campusx-official/langgraph-tutorials](https://github.com/campusx-official/langgraph-tutorials) | Progressive LangGraph notebooks + scripts | Practical workflows (BMI, essay, chatbot, tools, persistence, HITL, subgraphs, RAG, MCP) | Strong parallel track for Stage 04 |
| [campusx-official/chatbot-in-langgraph](https://github.com/campusx-official/chatbot-in-langgraph) | End-to-end chatbot project | Real chatbot with LangGraph features | Pair with Stage 04 tool-calling agent |
| [Yash-Kavaiya/CampusX-courses](https://github.com/Yash-Kavaiya/CampusX-courses) | Curated CampusX course collection | GenAI with LangChain, RAG, LlamaIndex, Vision GenAI, etc. | Supplemental project ideas and structured courses |
| This repo | Structured stages + must-do projects | Clear progression + production RAG guide | Work stages in order |

### Related (Your Ecosystem)

- [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path) — deeper LangGraph, HITL, MCP, multi-agent focus
- [Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith) — production RAG depth
- [mcp-learning-path](https://github.com/yash9614/mcp-learning-path)

**Recommended order:** Foundations (Stage 01 + sunnysavita early) → LangChain (Stage 02 + CampusX) → RAG (Stage 03 + sunnysavita RAG) → Agents/LangGraph (Stage 04 + CampusX LangGraph) → Advanced projects & fine-tuning.

---

## 🗺️ Recommended Unified Path

| Phase | Duration | Focus | Primary Resources (Direct) | This Repo Stage |
|-------|----------|-------|----------------------------|-----------------|
| **1. Foundations** | 1–2 weeks | NLP basics, embeddings, transformers intuition | sunnysavita Classes 1–15 · [Generative-AI-Indepth](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) · Stage 01 | `01-Foundations` |
| **2. LangChain Basics** | 1 week | Chains, prompts, memory, LCEL, structured output | [campusx langchain-models](https://github.com/campusx-official/langchain-models) · [langchain-prompts](https://github.com/campusx-official/langchain-prompts) · Stage 02 | `02-LangChain-Basics` |
| **3. RAG Systems** | 1–2 weeks | Document Q&A → production (hybrid, rerank, eval) | sunnysavita Classes 29–39 · [Generative-AI-Indepth](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) · Stage 03 + PRODUCTION-RAG-GUIDE | `03-RAG-Systems` |
| **4. Agents & LangGraph** | 1–2 weeks | Tool calling, stateful agents, routing, HITL | [campusx langgraph-tutorials](https://github.com/campusx-official/langgraph-tutorials) (esp. 9–15) · [chatbot-in-langgraph](https://github.com/campusx-official/chatbot-in-langgraph) · Stage 04 | `04-Agents-and-LangGraph` |
| **5. Advanced Projects** | 1 week | Multi-agent, SQL chat, search | Stage 05 · CampusX GenAI projects | `05-Advanced-Projects` |
| **6. Fine-tuning (Optional)** | Optional | Hugging Face, LoRA, etc. | sunnysavita Classes 18–28 · Stage 06 | `06-Fine-tuning-HuggingFace` |

---

## 🏆 Must-Do Projects (With Direct Links)

Complete in order. Full details in [MUST-DO-PROJECTS.md](MUST-DO-PROJECTS.md).

| # | Project | Skills | Direct Links to Start |
|---|---------|--------|-----------------------|
| 1 | Stateful Chatbot with Memory | Memory, session isolation, LCEL | Stage 02 `chatbots-with-memory.ipynb` · [campusx 9_basic_chatbot](https://github.com/campusx-official/langgraph-tutorials/blob/main/9_basic_chatbot.ipynb) |
| 2 | LangGraph Tool-Calling Agent | Tools, conditional edges, ReAct | Stage 04 `langgraph-chatbot-with-tools.ipynb` · [campusx 11_tools](https://github.com/campusx-official/langgraph-tutorials/blob/main/11_tools.ipynb) · [chatbot-in-langgraph](https://github.com/campusx-official/chatbot-in-langgraph) |
| 3 | Conversational / Production RAG | Hybrid search, rerank, eval, citations | Stage 03 + [PRODUCTION-RAG-GUIDE.md](03-RAG-Systems/PRODUCTION-RAG-GUIDE.md) · [sunnysavita Generative-AI-Indepth](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) · [campusx 13_rag](https://github.com/campusx-official/langgraph-tutorials/blob/main/13_rag.ipynb) |
| 4 | LangGraph + Vector Store Routing | Conditional routing + RAG | Stage 04 routing examples · CampusX workflows |
| 5 | Chat with SQL | Structured data tools | Stage 05 · CampusX practical projects |
| 6 | CrewAI Multi-Agent System | Multi-agent orchestration | Stage 05 · sunnysavita multi-agent classes |

---

## 🔑 Concept Cheat Sheet (With Jump Links)

| Term | One-Liner | Jump To |
|------|-----------|---------|
| **Embeddings** | Dense vector representations of text | sunnysavita early classes · Stage 01 |
| **LCEL** | LangChain Expression Language for composing runnables | Stage 02 · [campusx langchain-models](https://github.com/campusx-official/langchain-models) |
| **RAG** | Retrieve relevant chunks → augment prompt → generate | Stage 03 · [sunnysavita Generative-AI-Indepth](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance) |
| **Hybrid Search + RRF** | Dense + sparse (BM25) merged robustly | Stage 03 PRODUCTION-RAG-GUIDE · sunnysavita practical RAG |
| **Reranking** | Cross-encoder re-scores top candidates | Stage 03 · sunnysavita |
| **StateGraph** | Explicit graph of nodes + edges over shared state | Stage 04 · [campusx langgraph-tutorials](https://github.com/campusx-official/langgraph-tutorials) |
| **Tool Calling** | LLM decides when/how to call functions | Stage 04 · [campusx 11_tools](https://github.com/campusx-official/langgraph-tutorials/blob/main/11_tools.ipynb) |
| **Checkpointer / Memory** | Persist state across turns | Stage 02/04 · [campusx 10_persistence](https://github.com/campusx-official/langgraph-tutorials/blob/main/10_persistence.ipynb) |
| **HITL** | Interrupt for human approval | [campusx 14_hitl](https://github.com/campusx-official/langgraph-tutorials/blob/main/14_hitl.ipynb) |
| **Subgraph** | Nested graph for modularity | [campusx 15_subgraphs](https://github.com/campusx-official/langgraph-tutorials/blob/main/15_subgraphs.ipynb) |

---

## 🛠️ Practical Setup

```bash
uv sync   # or uv add langchain langchain-openai langgraph chromadb python-dotenv
cp .env.example .env   # if present; otherwise create one
# Add OPENAI_API_KEY, optional GROQ / HF / LANGCHAIN keys
uv run jupyter lab
```

- Prefer `uv`.
- Never hardcode keys.
- Start with cheaper models (`gpt-4o-mini`).
- Enable LangSmith tracing early for agents and RAG.

---

## 📎 Quick Links

- [MUST-DO-PROJECTS.md](MUST-DO-PROJECTS.md)
- [sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0](https://github.com/sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0)
- [sunnysavita10/Generative-AI-Indepth-Basic-to-Advance](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance)
- [campusx-official/langgraph-tutorials](https://github.com/campusx-official/langgraph-tutorials)
- [campusx-official/chatbot-in-langgraph](https://github.com/campusx-official/chatbot-in-langgraph)
- [campusx-official/langchain-models](https://github.com/campusx-official/langchain-models)
- [Yash-Kavaiya/CampusX-courses](https://github.com/Yash-Kavaiya/CampusX-courses)
- [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path) (deeper agentic focus)
- [Ultimate RAG Bootcamp](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith)

---

**Last updated:** 21 November 2026  
**Purpose:** Cross-repo compass for the Generative AI Learning Path. Update when new high-signal notebooks appear.

Happy learning! Start with `01-Foundations/README.md` and this map. 🤖
