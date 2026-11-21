# 02 - LangChain Basics

Master the core abstractions before building agents.

## Key Topics
- Chat models and prompts (OpenAI SDK vs LangChain wrappers)
- LCEL (LangChain Expression Language)
- Message history and stateful conversations
- Session management
- Message trimming
- Pydantic models for structured output

## Telusko Course Mapping
- `Calling Your First LLM` — raw OpenAI calls, system/human messages
- `Getting Started with LangChain 23-08-2026` and `Part-2`
- `Data Modeling with Pydantic` — structured output

Use `uv` for environments (preferred over plain venv in the course).

## Must-Do Notebook
- `chatbots-with-memory.ipynb` — Complete this first.

## What you should be able to do after this section
- Build a chatbot that remembers previous messages within a session.
- Use prompt templates correctly.
- Understand how to pass configuration (session_id) into a chain.
- Produce structured output with a Pydantic model.

**Next:** `03-RAG-Systems`.
