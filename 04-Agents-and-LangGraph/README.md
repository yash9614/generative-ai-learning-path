# 04 - Agents and LangGraph

Move from simple chains to **stateful agents** that can use tools and make decisions.

## Key Ideas

- Tools / function calling (OpenAI function calling + LangChain `@tool`)
- StateGraph, nodes, edges, conditional routing (`tools_condition`)
- ReAct-style loops
- Parallel nodes + reducers
- Subgraphs (as node or invoke)
- Human-in-the-loop (interrupts, parallel interrupts, tool interrupts)
- Checkpointers (InMemorySaver, SqliteSaver)
- Commands (`update` / `goto` / `resume`)
- Send / map-reduce, dynamic nodes
- Workflow patterns: prompt chaining, parallelization, routing, orchestrator-worker, evaluator-optimizer
- Multi-agent: supervisor, handoffs, deep agents
- Streaming modes (values, debug, checkpoint, tasks, messages)

## Complementary Resources

- Progressive notebooks: [sourangshupal/langraph-tutorials](https://github.com/sourangshupal/langraph-tutorials)
- Hands-on + diagrams: [d-hackmt/langgraph-life](https://github.com/d-hackmt/langgraph-life)
- Clean concept extract (hybrid RAG, LangGraph + MCP, multi-agent, GraphRAG): [PYTHON-FOR-GENAI-CONCEPTS.md](https://github.com/yash9614/agentic-ai-learning-path/blob/main/reference/PYTHON-FOR-GENAI-CONCEPTS.md)

## Telusko Course Mapping

- `LangChain Tools and Agents`, `Tool Calling (Part-2)`
- `Getting Started with LangGraph 17-10-2026`
- `Types of Graphs` series (18-10 through Part 4)
- `Advance LangGraph 14-11-2026` and `(part - 2) 15-11-2026` (agents project)
- `Agents in Langgraph 21-11-2026` (programs 1–21: streaming modes, human approval, plan-and-execute, supervisor, handoffs, orchestrator-workers, deep agent)
- `Agentic AI Final Project 22-11-2026` (multi-agent supervisor + RAG with pgvector + MCP tools + short/long-term memory in Postgres + FastAPI + frontend)

## Must-Do Notebooks

1. `getting-started-langgraph.ipynb`
2. `langgraph-chatbot-with-tools.ipynb` ← Highest priority

## What you should be able to do

- Build a graph that decides when to call a tool.
- Stream intermediate steps.
- Add a new tool and update the graph.
- Handle parallel writes with a reducer and pause for human approval.
- Implement at least one classic workflow pattern (e.g. orchestrator-worker).
- Understand a multi-agent supervisor that routes to specialists (RAG, tools via MCP, per-user store).

**Next:** Advanced projects. For deeper agentic patterns see the companion [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path).
