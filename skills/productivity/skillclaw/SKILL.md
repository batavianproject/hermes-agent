---
name: skillclaw
description: Use for collective AI agent skill evolution.
category: productivity
---

# SkillClaw Skill

SkillClaw is an agentic evolver that allows AI agent skills to evolve collectively from every real interaction. It enables experience to compound across sessions, agents, devices, and users, ensuring that skills keep growing silently in the background.

## 🎯 Core Concept: Collective Evolution
Unlike static skills, SkillClaw implements a continuous learning loop. Every interaction becomes a learning opportunity, allowing the agent to refine its procedures and knowledge based on real-world success and failure.

## 🛠️ Setup & Installation
To enable SkillClaw on your system:

1. **Install:** Use the shell installer (macOS/Linux) or the manual Python installation path (Windows).
2. **Configure:** Run `skillclaw setup` to initialize the client configuration.
3. **Start:** Execute `skillclaw start --daemon` to run the evolver in the background.

## ⌨️ Key Commands

### System Management
- `skillclaw status`: Checks if the evolver is running and healthy.
- `skillclaw config show`: Displays current upstream URL, model, and sharing target.
- `skillclaw config <key> <value>`: Updates a specific configuration setting.

### Skill Synchronization
- `skillclaw skills pull`: Downloads shared skills from the collective pool.
- `skillclaw skills push`: Uploads local evolved skills to the collective.
- `skillclaw skills sync`: Performs a bidirectional synchronization of skills.
- `skillclaw skills list-remote`: Browses available shared skills.

## 🔄 Workflow: The Evolution Loop
SkillClaw operates silently. The general flow is:
1. **Interaction:** The user chats with the agent.
2. **Experience:** The agent performs a task and receives feedback/results.
3. **Evolution:** The Agentic Evolver analyzes the interaction and updates the relevant skill.
4. **Collective Share:** Updated skills are pushed to a shared pool, benefiting all agents in the network.

## 🔌 Compatibility
SkillClaw is natively compatible with:
- **Hermes Agent**
- **OpenClaw / IronClaw / NanoClaw**
- **Claude Code / Cursor / Copilot**
- Any OpenAI-compatible API.

## ⚠️ Operational Note
Skill evolution happens silently. You do not need to manually trigger "learning" sessions; just interact with the agent as usual, and the experience will compound over time.
