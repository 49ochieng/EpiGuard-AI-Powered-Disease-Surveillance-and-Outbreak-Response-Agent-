
# HealthGuard: AI-Powered Disease Surveillance and Outbreak Response Agent

## Overview

**HealthGuard** is an AI-powered **Copilot Studio agent** designed to revolutionize disease surveillance, health data analysis, and outbreak management. Developed for the **Microsoft AI Agents Hackathon**, HealthGuard harnesses the full power of Microsoft's ecosystem to deliver a **proactive, intelligent, and secure public health assistant** that supports real-world healthcare workflows.

---

## Flow Diagram

![image](https://github.com/user-attachments/assets/107ce54e-441f-4ef5-80c2-6fd73085dbbd)


---

## Problem Statement

Health organizations face growing challenges in detecting, responding to, and managing disease outbreaks in real time. Data is scattered across platforms — emails, scanned reports, structured datasets, handwritten notes — making early detection slow and unreliable. Human workloads limit rapid case analysis, and critical decisions are often delayed.

---

## Solution: HealthGuard

HealthGuard solves this by orchestrating a network of intelligent automation and AI-powered tools to:

- Ingest and analyze various health documents (PDFs, Word, scanned images, emails)
- Summarize and extract key health indicators
- Predict outbreak risks and escalate urgent cases
- Automate task assignments and notifications
- Provide personalized, secure, and human-like interaction

---

## Architecture Diagram

![image](https://github.com/user-attachments/assets/83f51b65-e3ec-416f-878e-1e372f72c76a)


---

## Hackathon Alignment

HealthGuard is built specifically to align with the **Microsoft AI Agents Hackathon** objectives:

- **Copilot Studio Integration**: Custom topics, memory, actions, error handling, and channel publishing.
- **Agent Orchestration**: Triggers and orchestrates other flows, agents, and APIs.
- **Autonomous Execution**: Performs actions like summarization, escalation, reporting, and document management without user input.
- **Real-World Impact**: Targeted for health agencies, NGOs, and research bodies with strong practical benefits.
- **Security & Compliance**: Implements strict access controls aligned with Microsoft’s responsible AI practices.

---

## Technologies Used

- **Microsoft Copilot Studio** – Core conversational AI engine  
- **Power Automate** – Flow automation and integration  
- **SharePoint** – Document storage, knowledge base, and output destination  
- **Microsoft Planner** – Task assignment and escalation  
- **Microsoft Teams** – Publishing and end-user experience  
- **Azure OpenAI / GPT** – Document summarization and natural language understanding  
- **Microsoft Graph API** – On-prem file access and graph connector integration  
- **Dataverse** – Structured data ingestion and querying  
- **OCR (AI Builder / Flow)** – Extraction from scanned and handwritten health reports  

---

## Key Capabilities

### 1. OCR-Based Report Ingestion

When new documents (PDFs, images, scanned forms) are uploaded to SharePoint, HealthGuard triggers an OCR flow that:

- Extracts data from typed or handwritten reports  
- Summarizes findings using GPT  
- Adds the document to the searchable knowledge base  

> **Why OCR?** Healthcare data comes in all forms — including paper-based handwritten documents. With OCR, EpiGuard ensures all health records are usable regardless of origin.

---

### 2. Autonomous Email Integration

- Monitors a designated inbox
- Extracts attachments
- Summarizes using GPT
- Sends summary to researchers
- Saves file to secure file share

---

### 3. On-Prem Data Access

Via **Microsoft Graph Connector**, HealthGuard can:

- Read from local folders  
- Store attachments to on-prem file shares  
- Extend visibility beyond cloud environments  

![image](https://github.com/user-attachments/assets/6a5a1433-6288-4945-ac17-2090f3d1fc45)


---

### 4. Multi-Source Intelligence

HealthGuard pulls data from:

- SharePoint Libraries  
- OneDrive  
- Dataverse  
- File Shares  
- Web Search  
- Uploaded Files  
- Emails  
- Azure OpenAI Models  

![image](https://github.com/user-attachments/assets/23152c8b-cf42-480d-9205-5909418e718e)


---

### 5. Task Management + Notifications

- Auto-create tasks in Microsoft Planner  
- Escalate urgent issues via Teams or email  
- Option to save responses as DOCX and email  
- Auto-generate tickets and deadlines  

---

### 6. Security & Compliance

- Enforces **Sensitivity Labels**  
- Excludes **Confidential/Highly Confidential** content  
- Built-in Responsible AI policies and governance  

---

### 7. Advanced Comparisons

- Compare multiple reports in tabular format  
- Highlight key differences (symptoms, cases, locations)  
- Provide side-by-side summaries and recommendations  

---

### 8. User-Friendly and Personalized

- Greets by name and adjusts tone to time of day  
- Friendly error handling  
- Remembers context  
- Simple and accessible UI  

---

### 9. Channel Integration

- Available in **Microsoft Teams**  
- Seamless on desktop and mobile  

![image](https://github.com/user-attachments/assets/4ee2bf33-583a-4fec-9d52-206404e4ab76)


---

## Impact & Advantages

- ✅ **Faster Outbreak Detection** – Reduces manual work  
- ✅ **Real-Time Decision Support** – Converts raw data into insight  
- ✅ **Document-Agnostic** – Emails, PDFs, Word, Excel, Handwriting  
- ✅ **Scalable** – From clinics to national health authorities  
- ✅ **Secure & Compliant** – Data sensitivity built-in  

---

## Implementation Guide

### Prerequisites

- Power Platform Environment  
- Admin access to Power Apps & Copilot Studio  
- Microsoft Teams Admin Access  

---

### Step-by-Step Setup

1. **Download the Zipped Solution**  
   GitHub repo → `Deployment` folder → `EpiGuardSolution.zip`

2. **Import into Power Apps**  
   - Go to **Power Apps** → **Solutions** → **Import**  
   - Upload `.zip` file (Managed – not editable)

   ![image](https://github.com/user-attachments/assets/a32a5c57-b5a7-4d03-aef4-64ac09162c1d)


3. **Launch Copilot Studio**  
   - Open imported solution  
   - Click the agent to go to Copilot Studio  

4. **Configure & Publish Teams Channel**  
   - Navigate to **Channels**  
   - Select **Microsoft Teams**  
   - Click **Allow** → Submit for approval
   ![image](https://github.com/user-attachments/assets/1a8beeb5-27a0-4bd1-b0ba-2099ffce9e45)
5.	**Teams Admin Portal Approval**
  - The bot will appear in the Teams admin portal.
  - An admin can approve it for specific users or make it available to everyone.
![image](https://github.com/user-attachments/assets/36856072-8b56-4248-ba43-f61ed6ccc5fc)

 
6.	Teams User Access
 - Once approved, the agent will be live in the user’s Teams app.
 - Users can start chatting immediately using starter prompts.


---

## GitHub Repository Structure

```
/HealthGuard-copilot
├── README.md
├── solution/
│   └── HealthGuardSolution.zip
├── flows/
│   ├── OCRFlow.json
│   └── EmailProcessingFlow.json
├── samples/
│   ├── Outbreak_Report_Week14.docx
│   ├── Outbreak_Report_Week15.docx
│   └── Surveillance_CaseData_April2025.csv
├── docs/
│   └── HealthGuardArchitecture.png
└── prompts/
    └── starter-prompts.json
```

---

## Conclusion

**HealthGuard** is not just a chatbot. It’s an **autonomous, intelligent, and secure health assistant** that brings together the full Microsoft ecosystem to solve real-world disease surveillance challenges. From OCR to outbreak detection, document analysis to task management — EpiGuard is built to deliver meaningful impact.

> **Built with Copilot Studio.**

---

## License

**MIT License © 2025**

Permission is granted, free of charge, to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of this software and associated documentation files under the following conditions:

- The original copyright and license notice 
  must be included in all copies.
- The software is provided **"as is"**, without warranty of any kind.
- The authors are **not liable** for any damages arising from its use.
