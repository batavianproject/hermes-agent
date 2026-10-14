---
name: minions
description: Use for managing and supervising multiple Hermes sessions.
category: productivity
---

# Minions Skill

Minions acts as a "Mission Control" for your Hermes Agent. It provides a centralized management layer for users who juggle multiple, long-lived agent sessions across various projects, allowing you to track status, manage metadata, and supervise task progress from a single board.

## 🎯 Core Capability: Session Supervision
Instead of losing track of various chat threads, Minions transforms each task into a persistent Hermes root session. 
- **Task Board:** A visual overview of where everything stands—identifying what is finished, what is stuck, and what requires immediate human attention.
- **Metadata Tracking:** Stores task status, settings, and metadata in a local SQLite database for fast retrieval and persistence.
- **Local-First Privacy:** Supports self-hosting with SQLite, ensuring your session data and metadata stay on your local machine without cloud dependency.

## 🛠️ Setup & Installation
Minions can be run as a local server to manage your Hermes agents:
- **Quick Start:** Use `npx minionsai` to launch the mission control interface.
- **Deployment:** Install via npm or run the pre-built binary to maintain a persistent supervision board.

## 🔄 Operational Workflow
When managing complex, multi-session work, follow this flow:
1. **Task Initiation:** Define a new task in Minions, which initializes a dedicated Hermes root session.
2. **Agent Execution:** The agent works on the task independently (e.g., long-term research or a complex coding project).
3. **Supervision:** The user monitors the Minions board to check the "health" of the session.
4. **Intervention:** If a task is marked as "stuck" or "needs review," the user jumps directly into that specific session to provide guidance.
5. **Completion:** Once the goal is reached, the task is marked as finished on the board.

## 🎯 Ideal Use Cases
- **Indie Founders:** Delegating research, operations, and coding to multiple specialized agent sessions.
- **Power Users:** Managing 10+ concurrent agent threads across different projects.
- **Long-lived Work:** Running tasks that take hours or days to complete and require periodic check-ins.

## ⚠️ Compatibility Note
Currently, Minions is optimized specifically for the **Hermes Agent** ecosystem. Integration with OpenClaw is on the roadmap.
