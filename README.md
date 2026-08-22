# 🤖 Autonomous AI-CRM & WhatsApp Growth Engine

An end-to-end autonomous Customer Relationship Management (CRM) system designed to automate lead generation, customer support, and sales pipelines using Agentic Workflows and WhatsApp API integration. 

## 🏗️ Architecture Overview

This project is built on a modern AI-native stack, focusing on execution speed, autonomous agents, and robust backend infrastructure. It leverages function calling to allow AI models to perform real-world actions directly on the database and via external communication channels.

### Core Stack:
*   **AI Orchestration:** Hermes Agent Framework, OpenRouter (Multi-LLM routing for cost/performance optimization).
*   **Database & Auth:** Supabase (PostgreSQL), Real-time subscriptions.
*   **Communication:** WhatsApp Business API (Webhooks).
*   **Infrastructure:** Custom Linux VPS managed via Termius.
*   **AI Assistance Tools:** Claude Code, v0, Lovable (Used for rapid UI prototyping and backend refactoring).

## ⚙️ Key Features

1.  **Autonomous Agentic Workflows:** Utilizing the Hermes Agent Framework to process incoming leads, categorize intent, and update the Supabase database automatically without human intervention.
2.  **Omnichannel WhatsApp Integration:** Two-way communication via WhatsApp Business API, allowing the AI agent to handle customer inquiries 24/7 and trigger outbound marketing messages.
3.  **Dynamic Function Calling:** The LLMs are not just chatbots; they utilize function calling to execute specific business tools (e.g., `check_payment_status`, `update_lead_stage`, `cross_reference_demographics`).
4.  **Secure VPS Deployment:** Fully deployed on a custom VPS environment, managing daemon processes, secure API gateways, and environment variables safely via SSH (Termius).

## 🚀 How It Works (Data Flow)

1.  **Ingestion:** A customer sends a message via WhatsApp.
2.  **Webhook Trigger:** The WhatsApp API sends a payload to the backend server hosted on the VPS.
3.  **Agent Processing:** The Hermes Agent receives the payload, analyzes the context using an LLM (via OpenRouter), and determines the necessary action.
4.  **Database Interaction:** The agent uses function calling to query or update the Supabase database (e.g., registering a new lead).
5.  **Execution & Response:** The agent formulates a reply and sends it back to the customer via the WhatsApp API.

## 🔒 Security & Privacy Note

This repository contains the architectural outline and structural examples of the system. To protect client confidentiality and proprietary business logic, sensitive API keys, database credentials, and core proprietary algorithms have been abstracted or removed. 

> *The system relies on a `.env` file for all secure configurations. See `.env.example` for the required variables.*

---
*Architected by [Vinicius Fernandes](https://www.linkedin.com/in/vinicius-fernandes-1b3a79361/) | AI-Native Full-Stack Engineer & AI Automation Specialist*
