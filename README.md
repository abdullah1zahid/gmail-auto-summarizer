# 📬 Gmail Auto-Summary System

An AI-powered automation system built with **n8n** that retrieves, filters, and summarizes daily emails into a professional, bilingual (English & Urdu) report.

## 📽️ Project Demonstration
* **Video Demo:** [Watch the Workflow in Action](https://drive.google.com/file/d/1p738CtIZ01n3NV1kXd2DE6VD7FRxJHQV/view?usp=drive_link)

## 🚀 Key Features
* **Daily Automation:** Automatically triggers every morning at a scheduled time via the **Schedule Node**.
* **AI Summarization:** Uses **OpenAI GPT-4o-mini** to generate concise bilingual summaries in Urdu and English.
* **Smart Filtering:** Custom search queries focus on primary emails and ignore junk, ads, or automated loops.
* **Professional Delivery:** Sends a beautifully formatted HTML report directly to your inbox.
* **Analytics Dashboard:** Automatically logs execution data (Date, Day, Email Count) into a Google Sheet.

## 🛠️ Technical Workflow & Nodes

### 1. Trigger & Data Ingestion
* **Daily Schedule:** The starting point that triggers the entire system at a specific time every morning.
* **Gmail (Fetch Important Emails):** Connects to the API and retrieves messages from the Inbox while filtering out noise.

### 2. Logic & AI Engine
* **If Node:** A safety check that filters out any messages sent by the automation itself to prevent infinite loops.
* **AI (Summarize Node):** Powered by **GPT-4o-mini**, this node reads the subject and snippet to create bilingual summaries.
* **Log Statistics:** Captures metadata like `date`, `day`, and `totalEmails` using n8n expressions.

### 3. Aggregation & Delivery
* **Aggregate All Summaries:** Combines all individual AI outputs into a single structured list.
* **Gmail (Send Summary Email):** Formats the list into a professional HTML report delivered to the user.
* **Email Analytics Dashboard:** Appends the log metadata into a **Google Sheet** for long-term tracking.

## 📊 Technical Analysis
| Component | Implementation |
| :--- | :--- |
| **Automation Engine** | n8n |
| **AI Model** | OpenAI GPT-4o-mini |
| **Storage** | Google Sheets |
| **Primary Language** | English & Urdu |

---
**Developer:** Abdullah Zahid    
**Certifications:** Microsoft Azure AI Fundamentals (AI-900)
