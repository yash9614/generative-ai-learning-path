# Production RAG Guide

**Naive RAG** = Retrieve + Generate.  
**Production RAG** = Better Retrieval + Better Context + Reliable Generation + Evaluation + Monitoring.

## Why Naive Fails
| Problem | Symptom | Fix |
|---------|---------|-----|
| Vocabulary mismatch | Right doc exists but not retrieved | Query rewrite + hybrid search |
| Irrelevant context | Noise in the prompt | Reranking + metadata filters |
| Broken chunks | Meaning split across boundaries | Recursive / structure-aware chunking + overlap |
| No quality signal | You don't know if it's working | Hit@K + LLM-as-judge |
| Unstable updates | Duplicate or missing chunks | Deterministic chunk IDs |

## Production Pipeline
```
User Query
   ↓
Query Rewrite / Expansion
   ↓
Hybrid Retrieval (dense + sparse)
   ↓
Metadata Filtering
   ↓
Reranking (cross-encoder)
   ↓
Context Optimization + Citations
   ↓
LLM Generation
   ↓
Evaluation / Logging / Guardrails
```

## Key Techniques (from modular scripts)

### 1. Ingestion & Stable IDs
- Load PDF/TXT/MD
- Add rich metadata (source, path, type, chunk_index)
- Generate deterministic IDs: `sha256(source_path | position | content)`
- Batch upsert into Pinecone (or any vector DB)
- Use namespaces for isolation

### 2. Chunking
- Prefer `RecursiveCharacterTextSplitter` (respects paragraphs → sentences → words)
- Always use overlap (150–200 chars typical)
- Structure-aware options: MarkdownHeaderTextSplitter, parent-child, semantic

### 3. Hybrid Search + Reciprocal Rank Fusion
```python
# Dense (Pinecone) + Sparse (BM25)
# Then RRF:
score[doc] += 1 / (k + rank)   # k usually 60
```
RRF is robust when the two retrievers disagree.

### 4. Metadata Filtering
Filter before or after retrieval:
```python
store.similarity_search(query, filter={"department": "support", "status": "active"})
```

### 5. Reranking
Retrieve top 20–50 with hybrid, then re-score with a cross-encoder (e.g. `BAAI/bge-reranker-v2-m3`) and keep top 5.

### 6. Query Transformation
Rewrite vague queries into clear search queries before embedding.

### 7. Citations
Return sources with the answer so users (and evaluators) can verify.

### 8. Evaluation
- **Retrieval**: Hit@K, MRR, nDCG against labeled questions
- **Generation**: LLM-as-judge for groundedness + relevance + score (1–5)
- Track latency, cost, and user feedback in production

### 9. Multimodal
Convert tables/charts into concise text descriptions before embedding so they become searchable.

## Stack Used in the Reference Scripts
- LangChain + LangChain-Pinecone
- Pinecone (vector store + embeddings)
- Groq (LLM)
- rank-bm25 + sentence-transformers (hybrid + rerank)
- Pydantic for structured judge output

## Interview Framing
- “How do you improve retrieval quality?” → Hybrid + RRF + reranking + query rewrite
- “How do you know your RAG is working?” → Evaluation set + LLM judge + monitoring
- “How do you keep the index fresh?” → Stable IDs + incremental upserts + namespaces
- “How do you reduce hallucinations?” → Citations + groundedness checks + better retrieval

## Must-Do Upgrade Path
1. Build basic RAG (load → chunk → embed → retrieve → generate)
2. Add stable IDs + metadata
3. Add hybrid search + RRF
4. Add cross-encoder reranking
5. Add a small evaluation set and measure Hit@5 + generation score
6. Add citations and query rewriting

This progression turns a demo into something you can confidently discuss in interviews and run for real users.
