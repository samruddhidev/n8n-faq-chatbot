KJSSE FAQ Chatbot

Overview

An AI-powered FAQ chatbot built using n8n, Google Gemini, and Google Sheets. The chatbot helps users get instant answers to common questions related to KJSSE academics, admissions, fees, hostel facilities, placements, and more.

Features

* AI-powered conversational chatbot
* Answers questions using a Google Sheets FAQ database
* Supports English, Hindi, and Hinglish
* Maintains conversation memory
* Logs unanswered questions automatically
* Collects user contact numbers for unresolved queries
* Built using a no-code/low-code workflow in n8n

Tech Stack

* n8n
* Google Gemini 2.5 Flash
* Google Sheets
* LangChain Agent

Workflow Architecture

User Message
↓
Chat Trigger
↓
AI Agent
├── Gemini 2.5 Flash
├── Memory Buffer
├── FAQ Google Sheet
└── Unanswered Queries Sheet
↓
Chat Response

Google Sheets Structure

FAQ Sheet

| Question                      | Answer                                         | Category  |
| ----------------------------- | ---------------------------------------------- | --------- |
| What are the college timings? | Classes are conducted from 8:00 AM to 5:00 PM. | Academics |

Unanswered Queries Sheet

| Customer Question                           | Mobile Number |
| ------------------------------------------- | ------------- |
| Is there an international exchange program? | 9876543210    |

Setup Instructions

1. Clone the repository

git clone https://github.com/your-username/kjsse-faq-chatbot.git

2. Import the workflow

* Open n8n
* Click Import Workflow
* Select workflow.json

3. Configure credentials

Add:

* Google Gemini API Credentials
* Google Sheets OAuth Credentials

4. Connect your Google Sheets

Replace:

* YOUR_FAQ_SHEET_ID
* YOUR_UNANSWERED_QUERIES_SHEET_ID

with your own Google Sheet IDs.

5. Activate the workflow

Enable the workflow and start chatting.

Key Capabilities

* Finds the closest FAQ match even if wording differs
* Responds in the user's preferred language
* Prevents AI hallucinations by relying on FAQ data
* Stores unanswered queries for manual follow-up
* Provides a friendly and professional user experience

Future Improvements

* Semantic Search using Vector Databases
* WhatsApp Integration
* Telegram Integration
* Admin Dashboard
* Analytics and Reporting
* Multi-department Knowledge Base

Author

Samruddhi

Built as an AI Automation and Workflow Project using n8n and Google Gemini.
