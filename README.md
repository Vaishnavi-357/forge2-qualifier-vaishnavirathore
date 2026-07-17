# ForgeBot: Academic & Fitness AI Companion
**Forge Edition 2 Qualifier Submission**  
**Author:** Vaishnavi Rathore (@Vaishnavi-357)

## Overview
ForgeBot is a fully autonomous AI agent built on the **OpenClaw** framework and powered by Google's Gemini 3.5 Flash reasoning engine. It operates natively within Slack as a continuous background daemon, designed to act as a highly capable academic tutor and a daily accountability partner.

## Core Capabilities
* **Socratic Academic Tutor:** Configured to assist with complex problem-solving matching the rigor of JEE Advanced mathematics (e.g., probability, calculus) and organic chemistry mechanisms. It guides the user through problems step-by-step rather than just printing the answers.
* **Daily Fitness Tracking:** Utilizes OpenClaw's persistent memory and autonomous Heartbeat to track physical activity goals. It logs daily step counts (targeting 10,000+ steps) from mobile step counters and calculates estimated calorie burn based on distance traveled.
* **Always-On Autonomy:** Configured as a native Windows Scheduled Task with a 30-minute Heartbeat interval, allowing the agent to check tasks, manage memory, and process information even when the user is offline.

## System Architecture & Tech Stack
* **Framework:** OpenClaw Agent Framework
* **LLM Engine:** Google Gemini API (Gemini 3.5 Flash)
* **Interface:** Slack API (Real-Time Messaging)
* **Deployment:** Native Windows Background Service

## Repository Structure
This repository contains the core configuration files that define the agent's personality, operational rules, and autonomous routines. *(Note: `openclaw.json` and API credentials are intentionally excluded for security).*
* `SOUL.md`: Defines the agent's core persona, academic rigor, and conversational tone.
* `AGENTS.md`: Operational instructions and tool routing.
* `USER.md`: User-specific context, goals, and metric targets.
* `HEARTBEAT.md`: The 30-minute interval scheduled task manifest.

## Setup Instructions (Local Deployment)
To run this agent on a new machine:
1. Install [OpenClaw](https://github.com/openclaw/openclaw).
2. Configure the Gemini API and Slack API credentials in `~/.openclaw/openclaw.json`.
3. Clone this repository and move the `.md` files into `~/.openclaw/workspace/`.
4. Run `openclaw gateway start` to initialize the background daemon.