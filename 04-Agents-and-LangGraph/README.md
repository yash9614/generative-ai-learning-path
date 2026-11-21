# 04 - Agents and LangGraph

Move from simple chains to **stateful agents** that can use tools and make decisions.

## Key Ideas
- Tools / function calling (OpenAI function calling + LangChain `@tool`)
- StateGraph, nodes, and edges
- Conditional routing (`tools_condition`)
- ReAct-style loops
- Parallel nodes + reducers
- Subgraphs (as node or invoke)
- Human-in-the-loop (interrupts, parallel interrupts, tool interrupts)
- Checkpointers (InMemorySaver, SqliteSaver)
- Commands (`update` / `goto` / `resume`)
- Send / map-reduce, dynamic nodes
- Workflow patterns: prompt chaining, parallelization, routing, orchestrator-worker, evaluator-optimizer

## Complementary Tutorial Resources

- **Progressive 10-notebook series**: [sourangshupal/langraph-tutorials](https://github.com/sourangshupal/langraph-tutorials)  
  01 intro → 02 conditional routing → 03 tools (OpenAI) → 04 persistence/memory → 05 HITL + streaming → 06 parallel + subgraphs → 07 production patterns → 08 Command / functional API / long-term memory → 09 multi-agent → 10 testing & observability

- **Hands-on notebooks + diagrams + interactive deck**: [d-hackmt/langgraph-life](https://github.com/d-hackmt/langgraph-life)  
  Basics, components (streaming, tools, ReAct, memory), debugging (Studio), workflows, HITL, agentic/corrective RAG, multimodal

## Telusko Course Mapping
- `LangChain Tools and Agents`, `Tool Calling (Part-2)`
- `Getting Started with LangGraph 17-10-2026`
- `Types of Graphs` series (18-10 through Part 4)
- `Advance LangGraph 14-11-2026` and `(part - 2) 15-11-2026` (including the `agents` project)

## Must-Do Notebooks
1. `getting-started-langgraph.ipynb`
2. `langgraph-chatbot-with-tools.ipynb` ← Highest priority

## What you should be able to do
- Build a graph that decides when to call a tool.
- Stream intermediate steps.
- Add a new tool and update the graph.
- Handle parallel writes with a reducer and pause for human approval.
- Implement at least one classic workflow pattern (e.g. orchestrator-worker).

**Next:** Advanced projects. For deeper agentic patterns see the companion [agentic-ai-learning-path](https://github.com/yash9614/agentic-ai-learning-path).
