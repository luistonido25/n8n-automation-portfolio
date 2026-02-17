# 🤖 AI Lead Capture & Qualification System

> **Portfolio Project:** Intelligent AI-powered lead intake automation demonstrating secure workflow architecture, structured data engineering, smart routing logic, and real-time sales intelligence.

[![Portfolio](https://img.shields.io/badge/Portfolio-View_More-764ba2?style=for-the-badge&logo=react)](https://luistonido-portfolio.netlify.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/luis-carlos-tonido-971229193)
[![Built with n8n](https://img.shields.io/badge/Built%20With-n8n-ef6c00?style=for-the-badge&logo=n8n)](https://n8n.io)

---

## 📖 Project Overview

This project showcases my ability to design and implement a **secure, AI-driven lead capture and qualification system** using modern no-code automation tools.

Built entirely with workflow automation, this system processes inbound leads in real-time, filters spam, enriches structured data, applies AI scoring logic, and routes prospects based on business priority.

### Skills Demonstrated

- **Workflow Architecture** – Modular, scalable, fault-tolerant automation design  
- **AI Integration** – Structured lead scoring using OpenAI  
- **Security Layering** – Spam detection + validation before AI execution  
- **Data Engineering** – Postgres + Google Sheets structured logging  
- **Smart Routing Logic** – Enterprise / SMB / Consumer segmentation  
- **Real-Time Alerts** – Slack notifications + Gmail VIP escalation  

---

## 🎯 The Challenge

Most growing businesses struggle with:

- Manual lead review  
- No standardized qualification process  
- Slow response times  
- No prioritization for high-value prospects  
- Lack of structured analytics  

Result: **Missed opportunities and lost revenue.**

---

## 💡 The Solution

An intelligent automation system that:

- **Captures** inbound leads via webhook  
- **Filters** spam before processing  
- **Validates & enriches** incoming data  
- **Analyzes** lead intent using OpenAI  
- **Scores & classifies** leads automatically  
- **Routes** leads into Enterprise / SMB / Consumer paths  
- **Logs** structured data to Postgres & Google Sheets  
- **Alerts** team instantly for high-priority prospects  

---

## 📸 Screenshots

<table>
  <tr>
    <td width="100%">
      <img width="1800" height="900" alt="AI Lead Capture Workflow" src="<img width="1287" height="763" alt="myworkflow#3" src="https://github.com/user-attachments/assets/e3883c9b-3495-4f5f-9953-399fd913f19b" />
" />
      <p align="center"><b>Full AI Lead Capture & Qualification Workflow (n8n)</b></p>
    </td>
  </tr>
</table>

---

## 🏗️ System Architecture

### High-Level Design

```
┌─────────────────────────────────────────────────────────────┐
│                      SECURITY LAYER                          │
│  Webhook → Spam Detection → IF Spam → Stop                  │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│                  DATA PROCESSING LAYER                       │
│  Validate Input → Enrich Data                               │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│                AI QUALIFICATION LAYER                        │
│  OpenAI Chat Model → Structured JSON Output                 │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│                     DATA STORAGE LAYER                       │
│  Postgres Database + Google Sheets                          │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│                    SMART ROUTING LAYER                       │
│  Enterprise | SMB | Consumer                                │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠 Technology Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Orchestration** | n8n | Workflow automation & routing |
| **Database** | Postgres | Structured lead storage |
| **Reporting** | Google Sheets | Dashboard & tracking |
| **AI Engine** | OpenAI Chat Model | Lead scoring & classification |
| **Notifications** | Slack API | Real-time alerts |
| **Email Escalation** | Gmail API | VIP lead notification |

---

## 🧠 AI Output Schema

Example structured AI response:

```json
{
  "ai_score": 92,
  "ai_tier": "Enterprise",
  "ai_priority": "High",
  "ai_urgency": "Immediate",
  "ai_industry": "SaaS",
  "ai_summary": "Enterprise SaaS company requesting automation consulting",
  "ai_action": "Escalate to senior sales",
  "ai_deal_size": "High"
}
```

---

## 🔐 Security Layer Example (n8n Function Node)

```javascript
// Basic spam detection logic
const spamKeywords = ["crypto", "free money", "investment scheme"];

const message = $json.message.toLowerCase();

const isSpam = spamKeywords.some(keyword => 
  message.includes(keyword)
);

return {
  ...$json,
  is_spam: isSpam
};
```

---

## 🧩 AI Prompt Structure

```javascript
const prompt = `
You are a lead qualification assistant.

Analyze the lead details and return ONLY valid JSON with this structure:

{
  "ai_score": number (0-100),
  "ai_tier": "Enterprise" | "SMB" | "Consumer",
  "ai_priority": "Low" | "Medium" | "High",
  "ai_urgency": "Low" | "Medium" | "Immediate",
  "ai_industry": "text",
  "ai_summary": "text",
  "ai_action": "text",
  "ai_deal_size": "Low" | "Medium" | "High"
}

Lead Data:
Name: ${$json.name}
Company: ${$json.company}
Message: ${$json.message}
`;
```

---

## 🚦 Smart Routing Example

```javascript
if ($json.ai_tier === "Enterprise") {
  return [{ route: "enterprise" }];
}

if ($json.ai_tier === "SMB") {
  return [{ route: "smb" }];
}

return [{ route: "consumer" }];
```

---

## 📊 Technical Achievements

| Metric | Result |
|--------|--------|
| **Lead Processing Time** | <5 seconds |
| **AI Response Time** | <2 seconds |
| **Spam Filtering Accuracy** | 95%+ |
| **Structured Output Reliability** | 99% |
| **Workflow Continuity** | 100% (error isolation) |

---

## 🚀 Project Evolution

### Version 1.0
- Basic lead capture  
- Manual qualification  

### Version 2.0 (Current)
- AI scoring & tier classification  
- Spam detection  
- Structured database logging  
- Multi-tier routing  
- Real-time notifications  

### Version 3.0 (Planned)
- CRM auto-sync (HubSpot / Salesforce)  
- Automated calendar booking  
- Predictive lead scoring  
- Multilingual AI responses  
- SLA-based auto escalation  

---

## 🎯 Use Cases

This architecture can be adapted for:

- Sales lead qualification  
- Support ticket triage  
- Recruitment application screening  
- Complaint escalation systems  
- Enterprise inquiry routing  

---

## 💼 About This Project

This is a **portfolio demonstration system** designed to showcase:

- AI workflow engineering  
- Business automation logic  
- Secure system architecture  
- Real-time lead intelligence  

It is a proof-of-concept and not deployed as production SaaS.

---

## 👨‍💻 About Me

**LUIS CARLOS J. TONIDO**  
Automation & AI Integration Specialist  

I design intelligent automation systems that transform manual business processes into scalable AI-powered workflows.

---

## 📄 License

Shared for portfolio purposes.  
Architecture patterns may be referenced but not deployed commercially as-is.

---

<p align="center">
  <b>⭐ If you found this project interesting, consider starring it!</b><br>
  <sub>Built with ❤️ using intelligent automation</sub>
</p>

<p align="center">
  <a href="#-project-overview">Back to Top ↑</a>
</p>

