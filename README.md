*# Telecom Sector AI Chatbot*



*## Conversational Design \& Requirement Analysis*



*\*\*Week 1 Task Deliverable — AI Chatbot Developer Internship\*\**



*This repository contains the Week 1 deliverables for an AI chatbot designed for the \*\*telecom sector\*\*. The project focuses on conversational design, customer requirement analysis, user personas, use-case modelling, intent and entity definition, conversational flow design, and NLP design decisions.*



*The proposed chatbot is intended to support customers across \*\*mobile applications, websites, and WhatsApp\*\*, while providing a clear path to human-agent escalation when self-service is unsuccessful or when the customer requests human assistance.*



*---*



*## 📌 Project Overview*



*Telecom customer-support systems receive a large number of repetitive queries related to billing, recharges, plans, network problems, SIM services, complaints, and general account information.*



*The objective of this project is to design the requirements and conversational architecture for an AI chatbot capable of handling common telecom customer inquiries through a structured, context-aware conversational experience.*



*The Week 1 analysis focuses on:*



*- Understanding common telecom customer inquiry categories*

*- Identifying user requirements and expectations*

*- Defining representative customer personas*

*- Designing important customer-support use cases*

*- Creating an intent and entity catalogue*

*- Designing conversational flows*

*- Defining NLP and conversational design decisions*

*- Establishing evaluation metrics*

*- Identifying assumptions, constraints, and risks*

*- Defining the next steps toward implementation*



*---*



*## 🎯 Objectives*



*The primary objectives of Week 1 are:*



*1. Analyze common telecom customer-support requirements.*

*2. Identify major categories of customer inquiries.*

*3. Define functional and non-functional chatbot requirements.*

*4. Develop representative user personas.*

*5. Create detailed chatbot use cases.*

*6. Define chatbot intents and entities.*

*7. Design conversational flows for major service areas.*

*8. Define NLP and conversational design strategies.*

*9. Establish measurable chatbot evaluation metrics.*

*10. Identify assumptions, constraints, and potential risks.*



*---*



*## 👥 Target Users*



*The conversational design considers four representative customer personas.*



*### 1. Budget-Conscious Student — Ananya Das*



*- Age: 20*

*- Service: Prepaid*

*- Digital comfort: High*

*- Preferred channels: WhatsApp / Mobile App*

*- Primary needs:*

&#x20; *- Fast recharge*

&#x20; *- Affordable plans and add-ons*

&#x20; *- Immediate payment confirmation*



*\*\*Design implications:\*\**

*- Fast recharge flow*

*- Price-sensitive recommendations*

*- Clear payment failure explanations*

*- Easy retry mechanism*



*---*



*### 2. Small-Business Owner — Rajesh Sarkar*



*- Age: 40*

*- Service: 6-line business postpaid*

*- Digital comfort: Medium*

*- Primary needs:*

&#x20; *- Multi-line billing*

&#x20; *- Add or suspend lines*

&#x20; *- Avoid service disruption*

&#x20; *- Human assistance when required*



*\*\*Design implications:\*\**

*- Multi-line account support*

*- Ticket ID and SLA information*

*- Simple escalation to a human agent*



*---*



*### 3. Senior Citizen — Meera Iyer*



*- Age: 68*

*- Service: Prepaid*

*- Digital comfort: Low*

*- Preferred channels: WhatsApp / Voice*

*- Primary needs:*

&#x20; *- Simple explanations*

&#x20; *- Safe recharge*

&#x20; *- Quick access to human support*



*\*\*Design implications:\*\**

*- Plain-language responses*

*- Clear OTP trust messaging*

*- Persistent human-agent option*



*---*



*### 4. Tech-Savvy Heavy Data User — Karan Agarwal*



*- Age: 26*

*- Service: Postpaid*

*- Digital comfort: Very High*

*- Primary needs:*

&#x20; *- Network diagnostics*

&#x20; *- Personalized plans*

&#x20; *- Self-service troubleshooting*

&#x20; *- Conversational ticket tracking*



*\*\*Design implications:\*\**

*- Automated diagnostic checks*

*- Usage-based plan recommendations*

*- Conversational ticket-status functionality*



*---*



*## 📞 Major Customer Inquiry Categories*



*The Week 1 analysis identifies six major telecom customer inquiry domains:*



*| Category | Examples |*

*|---|---|*

*| Billing \& Payments | Bill amount, payment, invoice, billing dispute |*

*| Plans \& Recharges | Recharge, plan inquiry, plan change, data add-on |*

*| Network \& Service Troubleshooting | No internet, slow data, network problems |*

*| SIM \& Number Services | SIM activation, SIM replacement, porting |*

*| Complaints \& Feedback | Complaint registration, complaint status, feedback |*

*| General / Account Information | Account information and general FAQs |*



*---*



*## ⚙️ Functional Requirements*



*The proposed chatbot should support:*



*- User authentication*

*- Intent classification with confidence scoring*

*- Entity extraction*

*- Backend/API integration*

*- Multi-turn conversational context*

*- Quick replies and menu-based interaction*

*- English and one regional language*

*- Human-agent escalation*

*- Conversation and interaction logging*

*- Outbound confirmations*



*### Backend Integration Areas*



*The proposed architecture considers integration with:*



*- Billing / CRM systems*

*- BSS / OSS systems*

*- Payment Gateway*

*- Number Portability Database*

*- Identity / KYC Verification System*



*---*



*## 🔐 Non-Functional Requirements*



*The proposed chatbot should consider:*



*- \*\*Availability:\*\* 99.5%*

*- \*\*Latency:\*\* p95 under 2 seconds for standard intents*

*- \*\*Security:\*\* Encryption, PCI-DSS and applicable regulatory requirements*

*- \*\*Scalability:\*\* Horizontal scalability*

*- \*\*Auditability:\*\* Appropriate logging and audit trails*

*- \*\*Accessibility:\*\* WCAG 2.1 AA*

*- \*\*Extensibility:\*\* Support for future intents and services*

*- \*\*Omnichannel consistency:\*\* Consistent conversational state across supported channels*



*---*



*## 🧩 Use Cases*



*The Week 1 design contains seven major use cases.*



*| ID | Use Case |*

*|---|---|*

*| UC-01 | Check current bill / Pay online |*

*| UC-02 | Dispute billing charge |*

*| UC-03 | Upgrade / Downgrade mobile plan |*

*| UC-04 | Troubleshoot no internet / slow data |*

*| UC-05 | Check outage status |*

*| UC-06 | Activate new SIM / Port number |*

*| UC-07 | Escalate to human after failed self-service |*



*Detailed use-case documentation is available in:*



*`docs/use\_cases.md`*



*---*



*## 🧠 Intent \& Entity Catalogue*



*The chatbot design defines intents across three priority tiers.*



*### Tier 1 — Core Intents*



*- `greeting`*

*- `authentication\_otp`*

*- `billing\_inquiry`*

*- `bill\_payment`*

*- `plan\_inquiry`*

*- `plan\_change`*

*- `recharge`*

*- `network\_issue`*



*### Tier 2 — Important Intents*



*- `invoice\_download`*

*- `billing\_dispute`*

*- `data\_addon\_purchase`*

*- `balance\_check`*

*- `outage\_status`*

*- `sim\_activation`*

*- `number\_port\_in`*

*- `agent\_handoff\_request`*



*### Tier 3 — Additional Intents*



*- `auto\_pay\_setup`*

*- `sim\_replacement`*

*- `esim\_request`*

*- `complaint\_registration`*

*- `complaint\_status\_check`*

*- `feedback\_rating`*

*- `general\_faq`*

*- `goodbye`*



*`language\_preference` is treated as a cross-cutting conversational requirement.*



*The complete catalogue is available in:*



*`data/intent\_entity\_catalogue.csv`*



*> \*\*Note:\*\* The source Week 1 document describes the catalogue as a "22-intent catalogue" while its detailed listing contains additional system-level dialogue acts such as greeting and goodbye. These are treated separately from the core business-intent count in the project structure.*



*---*



*## 🔄 Conversational Flow Design*



*The repository contains six major conversational-flow diagrams.*



*### 1. Master Conversation Flow*



*The master flow handles:*



*1. Session start*

*2. Greeting*

*3. Authentication*

*4. Intent classification*

*5. Intent-specific routing*

*6. Resolution check*

*7. Conversation closure or escalation*



*---*



*### 2. Billing \& Payment Flow*



*The billing flow supports:*



*- Bill summary*

*- Online payment*

*- Invoice download*

*- Billing dispute*

*- Payment failure and retry*

*- Dispute ticket generation*



*---*



*### 3. Plan Upgrade / Change Flow*



*The plan flow includes:*



*- Usage retrieval*

*- Personalized plan recommendations*

*- Eligibility verification*

*- Customer confirmation*

*- BSS / OSS update*

*- Alternative options when the selected plan is unavailable*



*---*



*### 4. Network Troubleshooting Flow*



*The network flow follows a diagnostic-first approach:*



*1. Identify the network issue*

*2. Perform diagnostic checks*

*3. Check for known outages*

*4. Provide guided troubleshooting*

*5. Raise a support ticket if unresolved*

*6. Escalate to a human agent when necessary*



*---*



*### 5. SIM \& Number Services Flow*



*This flow covers:*



*- SIM activation*

*- Number porting*

*- e-KYC verification*

*- Service-specific processing*

*- SMS confirmation/reminders*



*---*



*### 6. Human-Agent Handoff Flow*



*Human escalation can be triggered by:*



*- Explicit customer request*

*- Low-confidence intent classification*

*- Negative sentiment*

*- Repeated failed attempts*

*- Unresolved self-service issues*



*Relevant conversation context should be packaged with the escalation so that the customer does not have to repeat the complete issue.*



*---*



*## 📂 Repository Structure*



*```text*

*telecom-ai-chatbot/*

*│*

*├── README.md*

*│*

*├── data/*

*│   └── intent\_entity\_catalogue.csv*

*│*

*├── diagrams/*

*│   ├── billing\_payment\_flow.png*

*│   ├── human\_handoff\_flow.png*

*│   ├── master\_conversation\_flow.png*

*│   ├── network\_troubleshooting\_flow.png*

*│   ├── plan\_upgrade\_flow.png*

*│   └── sim\_number\_flow.png*

*│*

*├── docs/*

*│   ├── Week\_1\_Requirement\_Analysis.docx*

*│   ├── nlp\_design.md*

*│   ├── use\_cases.md*

*│   └── user\_personas.md*

*│*

*└── references/*

&#x20;   *└── sources.md*

