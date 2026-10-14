---
name: agent-reach
description: Use for automated job search and career data extraction.
category: productivity
---

# Agent-Reach Skill

Agent-Reach is a powerful automation framework designed to extend an AI agent's reach into various career and professional platforms. It specializes in automated job searching, extracting detailed Job Descriptions (JD), and managing professional outreach across multiple channels.

## 🎯 Core Capabilities

### 1. Multi-Platform Job Searching
- **Channel-Based Access:** Supports a wide array of career platforms (e.g., Boss Zhipin and others).
- **Deep Search:** Ability to perform keyword-based job searches and retrieve full-text JDs.
- **Automated Extraction:** Efficiently scrapes job requirements, company info, and application details.

### 2. Advanced Browser Automation (CDP)
- **Real Browser Interaction:** Uses Chrome DevTools Protocol (CDP) to drive actual Chrome instances, ensuring higher reliability and better bot-bypass capabilities.
- **Session Management:** Handles complex login states and maintains sessions via browser cookies.
- **Direct Interaction:** Can navigate pages, click elements, and extract content exactly as a human would.

### 3. Agent-Guided Setup
- **Smart Configuration:** Includes a guided setup flow to ensure all dependencies (like specific Chrome versions and CDP ports) are correctly configured.
- **Health Checks:** Built-in `doctor` and `check()` functions to verify connection status and login state before attempting searches.

## 🛠️ Operational Workflow

When tasked with career research or job searching, Hermes should follow this sequence:
1. **Connection Probe:** Run `check()` to verify if the required channel is installed and the CDP port (e.g., 9222) is active.
2. **Auth Verification:** Check for valid session cookies. If `AUTH_EXPIRED` is detected, prompt the user for login/QR scan.
3. **Job Search:** Execute searches using the specific channel API (e.g., `search_jobs`).
4. **Data Retrieval:** Use `job_card_browser` or similar tools to extract the full content of a specific job posting.
5. **Synthesis:** Analyze the extracted JDs to match them with the user's profile or requirements.

## ⚠️ Important Constraints

- **Anti-Bot Challenges:** Be aware that platforms like Boss Zhipin may trigger security-check sliders. These are distinct from login states; the agent must notify the user to handle the slider manually.
- **CDP Dependency:** Most advanced channels require a dedicated Chrome instance running with a remote debugging port enabled.
- **Rate Limiting:** Respect the platform's throttling to avoid account suspension.

## 🧰 Key Tools
- `agent_reach check`: Verify connectivity and health.
- `agent_reach search`: Find jobs based on criteria.
- `agent_reach extract`: Get full JD content.
- `agent_reach doctor`: Comprehensive system diagnostic.
