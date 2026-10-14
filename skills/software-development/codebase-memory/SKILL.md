---
name: codebase-memory
description: Use for codebase indexing and graph queries.
category: software-development
---

# Codebase Memory (MCP)

Codebase Memory is a high-performance code intelligence system that indexes entire codebases into a persistent knowledge graph. Unlike standard text search or grep, this skill allows Hermes to understand the structural relationships, dependencies, and architecture of a project with extreme efficiency.

## 🎯 Core Capability: Knowledge Graph Indexing
Instead of reading files linearly, Codebase Memory creates a graph of the code.
- **Structural Awareness:** Understands how functions, classes, and modules relate across 158 different languages.
- **Extreme Efficiency:** Indexes average repositories in milliseconds and provides sub-millisecond query responses.
- **Token Optimization:** Reduces token usage by up to 99% by providing precise, targeted snippets of relevant code rather than large file dumps.
- **Zero Dependency:** Operates as a single static binary, making it lightweight and fast.

## 🛠️ Operational Workflow

When working with a large or unfamiliar codebase, Hermes should follow this sequence:
1. **Indexing:** Initialize the MCP server to index the target repository.
2. **Structural Querying:** Use the knowledge graph to answer complex architectural questions (e.g., "Where is this interface implemented?" or "What is the call chain for this function?").
3. **Targeted Extraction:** Retrieve only the specific code blocks identified by the graph for final analysis or modification.
4. **Persistence:** Leverage the persistent memory to avoid re-indexing the same codebase across different sessions.

## 🔍 When to Use This Skill
- **Architectural Mapping:** When you need to understand the "big picture" of a project.
- **Impact Analysis:** When changing a function and needing to know every single place in the project that will be affected.
- **Onboarding:** When entering a massive, unfamiliar codebase and needing to find the entry point or core logic quickly.
- **Token Saving:** When the codebase is too large to fit in the context window, but precise structural knowledge is required.

## ⚠️ Operational Note
Codebase Memory is an MCP (Model Context Protocol) server. For it to function, the MCP server must be configured and running in the Hermes environment. If queries fail, check the MCP server status via the system logs.
