---
name: composio-skills
description: Use for building agents with Composio Tool Router.
category: software-development
---

# Composio Skills

This skill provides a comprehensive set of best practices and guidelines for building AI agents using the Composio platform. It focuses on the Tool Router and Triggers systems, ensuring that agents are secure, scalable, and production-ready.

## 🎯 Core Capabilities

### 1. Tool Router (Agent Orchestration)
The Tool Router is the central hub for managing how an agent interacts with external tools.
- **Session Management:** Guidance on creating, managing, and isolating sessions to ensure user data security.
- **User ID Isolation:** Patterns for using unique User IDs to prevent cross-session data leakage.
- **Native vs. MCP:** Analysis of when to use native Composio tools versus Model Context Protocol (MCP) integrations.
- **Framework Integration:** Implementation patterns for various frameworks including Vercel, OpenAI Agents, LangChain, Claude, and CrewAI.

### 2. Triggers & Events (Real-time Automation)
Triggers allow agents to react to external events instead of just responding to prompts.
- **Event-Driven Architecture:** Creating and managing triggers for real-time webhooks.
- **Subscription Lifecycle:** Managing how agents subscribe to and unsubscribe from specific event streams.
- **Webhook Security:** Implementing verification and security checks for production-grade webhooks.

### 3. Authentication & Connectivity
- **Auth Flows:** Managing auto-authentication within chat interfaces versus manual authorization flows.
- **Connection UI:** Building interfaces that accurately reflect the connection status of various toolkits.

## 🛠️ Production Best Practices

When helping a developer build with Composio, Hermes should advocate for these patterns:
- **Security First:** Always prioritize User ID isolation and secure webhook verification.
- **Fail-Safe Handling:** Implement robust error handling for tool calls and trigger failures.
- **Deployment Guides:** Follow production deployment patterns to ensure stability in live environments.

## 🔄 Operational Workflow for Developers

When a user is building a Composio-powered agent, follow this sequence:
1. **Architectural Review:** Determine if the use case requires a simple Tool Router setup or a complex Trigger-based event system.
2. **Auth Setup:** Guide the user through the correct authentication flow (auto vs manual).
3. **Integration:** Provide the specific implementation pattern for the user's chosen framework (e.g., LangChain or Vercel).
4. **Testing:** Verify connection status and trigger firing using the Composio CLI or dashboard.
5. **Hardening:** Apply production patterns for security and error handling.

## 🧰 Key CLI Reference
- `composio login`: Authenticate the CLI.
- `composio whoami`: Check current organization and project context.
- `composio link`: Link the local environment to a Composio project.
- `composio manage`: Access the management namespace for tools and triggers.
