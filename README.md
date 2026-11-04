<h1 align="center">⚡ ERP Intelligence Bot ⚡</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=8A2BE2&center=true&vCenter=true&width=700&lines=ERP+Data+Automation;Commercial+Intelligence+System;Daily+Business+Insights;Built+with+n8n+%2B+LLMs" alt="Typing animation" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/n8n-Automation-111111?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n" />
  <img src="https://img.shields.io/badge/ERP-Data-8A2BE2?style=for-the-badge" alt="ERP data" />
  <img src="https://img.shields.io/badge/Telegram-Delivery-111111?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram" />
  <img src="https://img.shields.io/badge/AI-Insights-8A2BE2?style=for-the-badge&logo=openai&logoColor=white" alt="AI insights" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#impact">Impact</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#how-it-works">How It Works</a> •
  <a href="#setup">Setup</a> •
  <a href="#license">License</a>
</p>

---

## Overview

An automation system that generates and distributes daily commercial reports from ERP data. It turns raw data into information that supports business decisions.

## Impact

<p align="center">
  <img src="https://img.shields.io/badge/manual%20analysis%20saved-~20h%20per%20month-brightgreen?style=for-the-badge" alt="Time saved: ~20h per month" />
</p>

| Area | Result |
|---|---|
| **Manual analysis** | Roughly 20 hours per month removed |
| **Reporting** | Daily, fully automated delivery |
| **Monitoring** | Continuous detection of losses and opportunities |
| **Management** | Standardized indicators for decision-making |

## Architecture

<p align="center">
  <img src="https://github.com/user-attachments/assets/4e3d8c3c-7d14-4ed2-bed7-3256f9519b1a" width="90%" alt="Architecture diagram" />
</p>

## How It Works

The workflow runs daily on a schedule and follows this sequence:

```mermaid
flowchart TD
    A["⏰ Schedule Trigger"] --> B["🔌 ERP API<br/>/resumo-completo"]
    B --> C["📱 Telegram<br/>summary"]
    C --> D["🔌 ERP API<br/>/analise-comercial"]
    D --> E["📱 Telegram<br/>commercial analysis"]
    E --> F["🔌 ERP API<br/>/analise-abc"]
    F --> G["📈 ABC curve"]
    G --> H["🤖 OpenAI<br/>executive summary"]
    H --> I["📄 HTML report"]
    I --> J["✉️ Gmail"]
    J --> K["✅ Telegram confirmation"]
```

## Output (Telegram)

<p align="center">
  <img src="https://github.com/user-attachments/assets/4777b432-0f99-439e-83cd-7a8389e32ade" width="32%" alt="Telegram output example 1" />
  <img src="https://github.com/user-attachments/assets/c004011e-96af-4ca2-b796-df9bcc10abe3" width="32%" alt="Telegram output example 2" />
  <img src="https://github.com/user-attachments/assets/44b3a346-9bf8-45a6-b3a1-06888fc484ba" width="32%" alt="Telegram output example 3" />
</p>

## Tech Stack

| Tool | Role |
|---|---|
| **n8n** | Workflow orchestration |
| **ERP API** | Data source |
| **OpenAI** | Executive summaries |
| **Telegram** | Real-time delivery |
| **Gmail** | Report delivery |

## Design Decision

The core logic does not depend on AI. The LLM is used only to organize and summarize the data, while the critical analysis follows business rules.

## Setup

1. Import `erp-insights-workflow.safe.json` into n8n.
2. Configure credentials for the ERP API, OpenAI, Telegram, and Gmail.
3. Point the HTTP Request nodes to your ERP API.
4. Set the schedule in the Schedule Trigger node.
5. Activate the workflow.

## Security

Sensitive data and credentials have been removed from the workflow file. You will need to configure your own credentials during setup.

## License

Released under the [MIT License](LICENSE).

## Author

**Igor Henrique** · Automation • Data • Systems
