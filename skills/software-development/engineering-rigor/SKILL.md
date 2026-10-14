---
name: engineering-rigor
description: Use for engineering rigor and alignment. Avoid vibe coding.
category: software-development
---

# Engineering Rigor (Matt Pocock's Framework)

This skill implements a set of engineering patterns designed to eliminate "vibe coding" (coding based on intuition without verification) and replace it with rigorous alignment, explicit specifications, and verifiable results.

## 🎯 Core Philosophy: Alignment > Assumptions
The most common failure in AI-assisted development is the communication gap. The fix is a **Grilling Session**: getting the agent to ask detailed, probing questions about the plan before a single line of code is written.

## 🛠️ Key Engineering Patterns

### 1. The Grilling Session (`/grill-me`)
Instead of blindly executing a request, the agent relentlessly interviews the user until every branch of the design tree is resolved.
- **Goal:** Move from "I think I know what you want" to "I have a verified specification."
- **When to use:** Every time a significant change or new feature is proposed.

### 2. Two-Axis Code Review (`/code-review`)
Reviews are split into two parallel, independent axes to prevent pollution:
- **Axis A: Standards:** Does the code follow the repository's coding standards and avoid "Fowler smells" (code smells)?
- **Axis B: Spec:** Does the code faithfully implement the originating issue or specification?

### 3. Structured Handoffs (`/handoff`)
Compacts the current conversation into a high-density handoff document.
- **Goal:** Allow another agent (or a fresh session) to continue the work without losing critical context or decision history.

### 4. The Interactive Wizard (`/wizard`)
Generates an interactive Bash wizard to guide a human through steps the AI cannot perform (e.g., provisioning infra, setting secrets).
- **Goal:** Bridge the gap between agentic automation and human-required administrative tasks.

### 5. Explicit PR Shape (`/pr`)
Pull requests must follow a strict format:
- **Visual Summary:** The smallest visual evidence that makes the change clear.
- **Proof:** Before/After evidence that the change works.
- **Merge Danger:** Call out "one-way doors" (irreversible changes) and the "blast radius" of the change.

## 🔄 Operational Workflow
To apply engineering rigor, follow this loop:
1. **Align:** Run a `/grill-me` session to lock the spec.
2. **Implement:** Code based on the verified spec.
3. **Verify:** Run a two-axis `/code-review`.
4. **Document:** Create a structured `/pr`.
5. **Handoff:** Create a `/handoff` doc if switching agents/sessions.

## ⚠️ Guardrail: The "Wait-What" Trigger
If a message or instruction doesn't land, the agent should immediately re-pitch the request in plain English, using the project's `GLOSSARY.md` to resolve jargon.
