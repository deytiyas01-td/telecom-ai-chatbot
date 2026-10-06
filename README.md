# Telecom Sector AI Chatbot — Architecture & NLP Module Planning

**Internship Program:** AI Chatbot Developer (Telecom Sector) — Week 2 Deliverable  
**Prepared by:** Tiyas Dey  
**Academic Affiliation:** B.Tech, Computer Science & Engineering, University of Engineering & Management (UEM), Kolkata  
**Scope:** Week 2 — Chatbot Architecture, NLP Pipeline Design & Telecom Backend Integration  

---

## 📌 Executive Summary
This repository contains the system architecture specification, NLP processing pipeline configurations, and backend integration design for an enterprise-grade telecom AI chatbot. 

Building on Week 1 requirement analyses and conversational flows, this Week 2 design defines a **hybrid open-source NLP architecture** combining **Rasa Core** for dialogue management[cite: 1], **Hugging Face Transformers** (DistilBERT / MuRIL) for fine-tuned intent classification[cite: 1], and **spaCy** for hybrid entity extraction[cite: 1].

---

## 🏗️️ Core Architecture & Component Overview

The system is structured into five core decoupled layers[cite: 1]:

1. **Channel Layer:** Web Chat Widget, Mobile App, and WhatsApp Integration[cite: 1].
2. **API Gateway & Auth Layer:** TLS termination, rate-limiting, and OTP-based session state management[cite: 1].
3. **NLP Engine Layer:** Preprocessing, multi-language detection (handling English & code-mixed regional text), Intent Classification, and Named Entity Recognition (NER)[cite: 1].
4. **Dialogue & Orchestration Layer:** Slot tracking, business logic orchestration, and policy execution (RulePolicy + TEDPolicy)[cite: 1].
5. **Telecom Integration Layer:** Normalizes communication with legacy backends via middleware adapters equipped with retry circuits and caching[cite: 1].

---

## 🛠️ Recommended Technology Stack & Rationale

| Module / Layer | Technology Chosen | Technical Justification |
| :--- | :--- | :--- |
| **Dialogue Engine** | **Rasa Core** | Supports deterministic rule enforcement (OTP/KYC verification) alongside machine-learned dialogue policies (TED) for non-linear user branching[cite: 1]. |
| **Intent Classification** | **Hugging Face (`DistilBERT` / `MuRIL`)** | Fine-tuned transformers resolve fine-grained intent overlaps (e.g., `billing_inquiry` vs. `billing_dispute`)[cite: 1]. Google's `MuRIL` specifically handles code-mixed Indian regional inputs[cite: 1]. |
| **Entity Extraction** | **spaCy (`EntityRuler` + NER)** | High-speed regex pattern matching for fixed entities (`mobile_number`, `imei`, `port_code`) combined with statistical models for free-text parameters[cite: 1]. |
| **Response Generation (NLG)** | **Jinja2 Templates** | Ensures 100% precision and compliance in monetary and transactional messages, avoiding hallucination risks[cite: 1]. |

---

## 📑 Use Case Coverage (22 Catalogued Intents)

The architecture supports end-to-end processing across 7 core telecom use cases[cite: 1]:
* **UC-01:** Check Current Bill & Pay Online (`billing_inquiry`, `make_payment`)[cite: 1]
* **UC-02:** Dispute Invoice / Report Billing Error (`billing_dispute`)[cite: 1]
* **UC-03:** Network Troubleshooting & Outage Check (`troubleshoot_network`)[cite: 1]
* **UC-04:** Data Usage & Speed Issues (`check_data_balance`)[cite: 1]
* **UC-05:** Plan Change & Add-on Packs (`plan_change`, `activate_addon`)[cite: 1]
* **UC-06:** SIM Activation & MNP Porting (`sim_activation`, `mnp_status`)[cite: 1]
* **UC-07:** Human Agent Escalation (`escalate_human`)[cite: 1]

---

## 📁 Repository Structure

```text
telecom-ai-chatbot/
│
├── architecture/
│   └── Telecom_AI_Chatbot_Architecture_NLP_Module_Planning.docx   # Complete architectural design document
│
├── data/
│   ├── nlu.yml            # Seed training data for Tier 1 intents & code-mixed examples
│   └── domain.yml         # Rasa domain definitions (intents, entities, slots, actions)
│
├── src/
│   ├── adapters/          # Integration middleware for Billing, BSS/OSS, e-KYC, & Payment GW
│   ├── nlu/               # Custom transformer intent classifiers & spaCy pipelines
│   └── dialogue/          # Story rules and custom action handlers
│
├── config.yml             # Rasa + Hugging Face + spaCy pipeline configuration
├── requirements.txt       # Python environment dependencies
└── README.md              # Project documentation
