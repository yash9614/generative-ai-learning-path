# 03 - RAG Systems

Retrieval-Augmented Generation is the most practical skill for real applications.

## Core Pipeline (Naive)
1. Load documents
2. Split into chunks (with overlap)
3. Create embeddings
4. Store in a vector database
5. Retrieve top-k similar chunks for a query
6. Stuff the chunks into a prompt and generate an answer

## Production RAG (What Actually Ships)
Naive RAG breaks under real data and users. Production systems add:

- **Better retrieval**: Hybrid search (dense + BM25) + Reciprocal Rank Fusion
- **Query improvement**: Rewrite / expand before search
- **Filtering**: Metadata filters (status, department, date, region)
- **Reranking**: Cross-encoder to re-order top candidates
- **Context quality**: Citations, deduplication, compression
- **Evaluation**: Hit@K + LLM-as-judge (groundedness, relevance)
- **Operational hygiene**: Stable chunk IDs, batch upserts, namespaces, monitoring

**Full guide:** See [PRODUCTION-RAG-GUIDE.md](PRODUCTION-RAG-GUIDE.md) for the complete progression, patterns, and interview framing.

## Variations to explore
- Conversational RAG (with chat history)
- Hybrid search (dense + BM25 + RRF)
- Metadata filtering + reranking
- PDF / multimodal (tables & charts as text)
- Query transformation + citations
- Evaluation harness

## Recommended practice
Implement a small RAG system over your own documents, then upgrade it step-by-step to production quality (hybrid → rerank → eval).

**Next:** `04-Agents-and-LangGraph`.
