# AI Lead Capture & Qualification System — Portfolio

**One-line:** Intelligent multi-tier lead capture built with n8n, OpenAI, and Postgres — a production-ready automation that showcases architecture, integrations, and system design skills.

## What Problem Does This Solve?
Manual lead triage is slow, error-prone, and costly. Most businesses waste hours per day on:
- Filtering spam and junk submissions
- Validating and enriching lead data
- Qualifying leads by hand (reading, scoring, routing)
- Logging and reporting across multiple tools
- Notifying the right team members in real time

**This system automates the entire process end-to-end:**
- Instantly blocks spam and low-quality leads
- Validates and enriches every submission
- Uses AI to qualify, score, and segment leads (Enterprise/SMB/Consumer)
- Routes and notifies the right teams automatically
- Logs every action for analytics and compliance

**Estimated time saved:**
- Typical manual triage: 2–4 minutes per lead
- Automated: <5 seconds per lead
- For 100 leads/week: saves 3–6 hours/week (150–300 hours/year)

**Estimated money saved:**
- If a sales/admin rep costs $30/hour, this saves $4,500–$9,000/year in labor for 100 leads/week
- For higher lead volume or higher labor rates, savings scale up dramatically

> _No setup or deployment guide is included — this is a portfolio showcase, not a tutorial._

## Overview
This repository contains an end-to-end AI-driven lead capture and qualification workflow implemented in n8n. It demonstrates real-world automation patterns: webhook ingestion, spam protection, data validation & enrichment, LLM qualification, persistent memory, routing, and multi-channel notifications.

This is a portfolio piece — not a step-by-step tutorial. The goal is to showcase engineering decisions, integration skills, and system design for hiring managers and technical reviewers.

## Highlights / Skills Demonstrated
- n8n workflow design and orchestration (complex branching, IF nodes, webhooks)
- Integrations: OpenAI (LLM), Postgres (conversation memory), Google Sheets, Slack, Gmail
- Secure ingestion: spam detection, input validation, safe defaulting
- System design: multi-tier routing (Enterprise / SMB / Consumer) and audit logging
- Engineering practices: backups, non-destructive updates, scripted deployments
- JavaScript/Node: code nodes and maintainable transform logic

## Key Features
- Webhook-based lead ingestion with spam filtering and automatic rejection
- Structured AI qualification (JSON-only responses) with Postgres chat memory
- Tiered routing: Enterprise (VIP flow), SMB, Consumer — each with tailored responses
- Multi-channel logging: Postgres for persistence, Google Sheets for analytics, Slack/Gmail for alerts
- Non-blocking writes and error-tolerant branches (continueOnFail where appropriate)

## Architecture & Screenshot
Below is a visual overview of the workflow. Replace the placeholder image with a high-resolution screenshot of the n8n editor showing the workflow and color-coded sticky notes.

![Workflow overview](assets/screenshots/workflow.png)

(Place a screenshot at `assets/screenshots/workflow.png` in the repo.)

## Not a How-to
This README intentionally focuses on the architecture, design choices, and skills showcased. If you want a runnable guide or a deployment script added (for reviewers to run locally), tell me and I will add a concise `RUNNING.md` with exact steps.

## More About Me

- Portfolio: [https://luistonido-portfolio.netlify.app/](https://luistonido-portfolio.netlify.app/)
- LinkedIn: [www.linkedin.com/in/luis-carlos-tonido-971229193](https://www.linkedin.com/in/luis-carlos-tonido-971229193)

---
_Portfolio-ready snapshot — prepared for technical reviewers._
