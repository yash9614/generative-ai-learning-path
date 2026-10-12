# Must-Do Projects

Complete these projects in order. Each one builds skills needed for the next.

## 1. Stateful Chatbot with Memory
**Location:** `02-LangChain-Basics/chatbots-with-memory.ipynb`

**What you learn:**
- Using `ChatMessageHistory` and `RunnableWithMessageHistory`
- Session isolation with `session_id`
- Prompt templates with `MessagesPlaceholder`
- Trimming message history to control context length

**Challenge:** Add a system prompt that makes the bot answer in a specific style and persist language preference across turns.

---

## 2. LangGraph Tool-Calling Agent
**Location:** `04-Agents-and-LangGraph/langgraph-chatbot-with-tools.ipynb`

**What you learn:**
- Defining tools (Wikipedia, Arxiv)
- Binding tools to an LLM
- Building a StateGraph with nodes and conditional edges
- ReAct-style loop: chatbot → tools → chatbot
- Streaming intermediate steps

**Challenge:** Add a third tool (e.g., a simple calculator or web search) and update the routing logic.

---

## 3. Document Q&A / RAG Pipeline
Build or run a full RAG system:
1. Load documents (PDF or web)
2. Split into chunks
3. Embed (Hugging Face or OpenAI)
4. Store in a vector DB (Chroma or similar)
5. Retrieve relevant chunks
6. Generate answer with the retrieved context

**Challenge:** Add conversation memory so follow-up questions work.

---

## 4. LangGraph + Vector Store Routing
Route queries:
- If the question is about your documents → retrieve from vector store
- Otherwise → use external search (Wikipedia)

**What you learn:** Conditional routing in LangGraph + RAG integration.

---

## 5. Chat with SQL
Natural language → SQL query → answer over a SQLite database.

**What you learn:** Tool use for structured data, safety considerations around SQL generation.

---

## 6. CrewAI Multi-Agent
Define multiple specialized agents, assign tasks, and let them collaborate using tools.

**What you learn:** Multi-agent orchestration patterns.

---

### Tips for Success
- Run every notebook end-to-end.
- Modify something (change the model, add a tool, change the prompt).
- Write a short note for yourself explaining the data flow.
- Use LangSmith for tracing once you have a key.
