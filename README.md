# P08: Multilingual Helpdesk Model Router based on Cost, Latency and Privacy

**Course:** Generative AI and AI Platform Engineering (25CS2207E)  
**Institution:** Koneru Lakshmaiah Education Foundation (KLH) — Dept. of CSIT (II B.Tech, Academic Year 2026–2027)  
**Team ID:** T04  
**Supervisor:** Lakshmi Prasanna

---

## Team Members
| S.No | Name | Roll / ID Number |
| :--- | :--- | :--- |
| 1 | Bhargav | 2520090169 |
| 2 | Tarun | 2520090020 |
| 3 | Hanish | 2520090107 |

---

## Abstract
Modern enterprise helpdesks handle diverse user queries varying widely in linguistic complexity, response-time expectations, and data sensitivity. Routing every request to a single large proprietary Large Language Model (LLM) leads to unnecessary API expenditure, elevated tail latency, and potential exposure of Personally Identifiable Information (PII). This project implements a **Multilingual Helpdesk Model Router** supporting **English, Telugu, and Hindi** that dynamically inspects incoming queries for PII/privacy sensitivity, language tokenization overhead, and task complexity, and routes each request to the optimal backend—balancing local privacy-preserving open-weight models against fast and frontier cloud models via OpenRouter. The system logs per-request token usage, end-to-end latency, and cost metrics to provide verifiable cost-latency-privacy trade-offs.

---

## Repository Structure
* `/src` — Core routing engine, PII/complexity classifier, provider-agnostic LLM clients, and API service
* `/docs` — Architecture Decision Records (ADRs), system diagrams, and design documentation
* `/data` — Multilingual helpdesk evaluation prompts (English, Telugu, Hindi) and dataset references
* `/results` — Latency, token cost, and routing accuracy benchmark logs and charts
* `/reports` — Phase review reports, evaluation summaries, and final project documentation

---

## Setup and Execution Instructions
1. Clone the repository: `git clone https://github.com/Bhargava-007/KLH-CSIT-2026-27-T04-MultilingualModelRouter.git`
2. Enter the folder: `cd KLH-CSIT-2026-27-T04-MultilingualModelRouter`
3. Create and activate a virtual environment: `python -m venv .venv` and `.\.venv\Scripts\Activate.ps1`
4. Install dependencies: `python -m pip install -r requirements.txt`
5. Create a `.env` file in the root directory with `OPENROUTER_API_KEY=your_openrouter_api_key`
6. Run the application: `python src/main.py`

---

## Current Project Phase Status
* **Current Phase:** Phase 0 — Team Formation, Topic Selection (`P08`), & Repository Initialization
* **Completed:** Team formed (`T04`), project topic (`P08`) selected, and standardized repository structure initialized (`/src`, `/docs`, `/data`, `/results`, `/reports`).
* **Next Milestone (`review-1`):** Implement provider-agnostic LLM client (cloud + local) and baseline multilingual query dataset.