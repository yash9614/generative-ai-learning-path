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
- **Query improvement**: Rewrite / expand / decompose / multi-query before search
- **Filtering**: Metadata filters (status, department, date, region)
- **Reranking**: Cross-encoder to re-order top candidates
- **Context quality**: Citations, deduplication, compression
- **Evaluation**: Hit@K + RAGAS metrics (Faithfulness, Answer Relevancy, Context Precision/Recall, Answer Correctness) or LLM-as-judge
- **Operational hygiene**: Stable chunk IDs, SHA256 dedup, batch upserts, namespaces, monitoring

**Full guide:** See [PRODUCTION-RAG-GUIDE.md](PRODUCTION-RAG-GUIDE.md) for the complete progression, patterns, and interview framing.

## External Resources
- **Query transformations**: [d-hackmt/query-transformations](https://github.com/d-hackmt/query-transformations) (rewriting, step-back, multi-query + RRF, decomposition, routing, filters)
- **RAGAS evaluation**: [divesh-sse/RAGAS](https://github.com/divesh-sse/RAGAS) (metric isolation notebook + Streamlit demo)
- **Production toolkit**: [laxmimerit/RAGWire](https://github.com/laxmimerit/RAGWire) (multi-format → Qdrant, hybrid, LLM metadata, SHA256 dedup)
- **Local agentic RAG**: [laxmimerit/Agentic-RAG-with-LangGraph-and-Ollama](https://github.com/laxmimerit/Agentic-RAG-with-LangGraph-and-Ollama)

Full summary also lives in the companion agentic path: `reference/EXTERNAL-RAG-RESOURCES.md`.

## Variations to explore
- Conversational RAG (with chat history)
- Hybrid search (dense + BM25 + RRF)
- Metadata filtering + reranking
- PDF / multimodal (tables & charts as text)
- Query transformation + citations
- Evaluation harness (RAGAS or simple)

## Recommended practice
Implement a small RAG system over your own documents, then upgrade it step-by-step to production quality (query transform → hybrid → rerank → eval).

**Next:** `04-Agents-and-LangGraph`.
