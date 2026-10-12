# 03 - RAG Systems

Retrieval-Augmented Generation is the most practical skill for real applications.

## Core Pipeline
1. Load documents
2. Split into chunks (with overlap)
3. Create embeddings
4. Store in a vector database
5. Retrieve top-k similar chunks for a query
6. Stuff the chunks into a prompt and generate an answer

## Variations to explore
- Conversational RAG (with chat history)
- Hybrid search (dense + BM25)
- PDF querying
- Routing between different knowledge sources

## Recommended practice
Implement a small RAG system over your own documents (PDFs, notes, or a website).

**Next:** `04-Agents-and-LangGraph`.
