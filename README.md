# AI Expense Assistant using n8n + Telegram + Gemini

An AI-powered expense tracking assistant built using n8n, Telegram Bot, Gemini 2.5 Flash, Google Sheets, and Gmail.

This workflow allows users to send receipt images directly through Telegram. The AI agent extracts structured expense data, stores it in Google Sheets, and automatically triggers email alerts for high-value transactions.

---

# Features

* Receipt image expense extraction using AI
* Telegram Bot integration
* Automatic Google Sheets logging
* High-value expense alerts via Gmail
* Natural language expense queries
* AI agent workflow architecture
* Confidence scoring and review flags
* Multi-tool orchestration inside n8n

---

# Workflow Overview

User sends a receipt image or text message through Telegram.

The AI agent:

1. Extracts expense details from the receipt
2. Identifies vendor, amount, date, tax, category, and currency
3. Logs structured data into Google Sheets
4. Flags uncertain extractions for review
5. Sends Gmail alerts for expenses above $500
6. Replies back to the user on Telegram

---

# Tech Stack

* n8n
* Telegram Bot API
* Gemini 2.5 Flash
* Google Sheets API
* Gmail API

---

# Google Sheets Schema

The workflow logs expense data into a Google Sheets table with the following fields:

* LoggedAt
* TelegramUserId
* TelegramUsername
* ReceiptFileId
* Vendor
* ExpenseDate
* Currency
* Total
* Tax
* Category
* Notes
* Confidence
* NeedsReview
* MessageId
* Over500
* CFOEmailSentAt

---

# Workflow Architecture

Telegram Trigger
↓
AI Agent (Gemini 2.5 Flash)
↓
Google Sheets Logging
↓
Conditional Check (Expense > $500)
↓
Gmail Alert
↓
Telegram Confirmation Reply

---

# Example Use Cases

### Receipt Logging

User uploads a receipt image on Telegram.

The AI extracts:

* Vendor name
* Expense amount
* Currency
* Tax
* Date
* Expense category

The expense is automatically stored in Google Sheets.

---

### High-Value Expense Alerts

If the expense amount exceeds $500 USD:

* A Gmail alert is triggered
* CFO notification email is sent automatically

---

### Natural Language Queries

Users can ask:

* "How much did we spend on travel last month?"
* "Show expenses above $500"
* "Total food expenses this quarter"

The AI agent retrieves and summarizes data from Google Sheets.

---

# Learning Outcomes

This project helped explore:

* AI agent workflows
* Tool orchestration
* Workflow automation
* OCR + multimodal AI
* API integrations
* AI-powered business systems
* Structured data extraction
* Automation architecture design

---

# Note

This project was built for learning and experimentation with AI automation systems and agentic workflows.
