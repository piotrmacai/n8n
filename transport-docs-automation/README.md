🎯 Overview
This automation workflow eliminates manual data entry for transport documents by:

Monitoring Google Drive folders for new WZ documents (images/PDFs)
Extracting data using AI vision models (Google Gemini & OpenAI GPT-4 Vision)
Parsing structured information with LangChain AI agents
Validating against existing records to prevent duplicates
Storing data across multiple platforms (Google Sheets, Notion, Airtable)

Primary Use Case: Transportation and logistics companies processing delivery notes, bills of lading, and cargo manifests.
✨ Features
🤖 AI-Powered Data Extraction

Multi-Model Support: Google Gemini & OpenAI GPT-4 Vision
Intelligent OCR: Extracts text from images and PDFs
Structured Output Parsing: Consistent JSON schema using LangChain
Field Validation: Automatic data type conversion and validation

📊 Multi-Platform Storage

Google Sheets: Real-time spreadsheet updates
Notion Database: Structured database pages
Airtable: Record management with custom fields

🔍 Smart Duplicate Detection

Validates against existing records
Prevents duplicate entries
Human-in-the-loop approval for edge cases

📧 Email Integration

Gmail trigger for email attachments (optional)
PDF extraction from email attachments
Notification system for duplicates

🔄 Real-Time Processing

Google Drive folder monitoring (every minute)
Automatic image download and processing
Parallel multi-database updates

🏗️ Architecture
┌─────────────────────────────────────────────────────────────────┐
│                    TRIGGER SOURCES                              │
├──────────────────────┬──────────────────────────────────────────┤
│  Google Drive Monitor │    Gmail Attachment Monitor (Optional)  │
│  (Primary Trigger)    │    (Alternative Trigger)                │
└──────────┬────────────┴──────────────────┬─────────────────────┘
           │                               │
           ▼                               ▼
    ┌─────────────┐              ┌──────────────────┐
    │  Download   │              │  Extract PDF     │
    │  WZ Image   │              │  from Email      │
    └──────┬──────┘              └────────┬─────────┘
           │                               │
           └───────────────┬───────────────┘
                           ▼
                  ┌─────────────────┐
                  │  Analyze Image  │
                  │  (Gemini Vision)│
                  └────────┬────────┘
                           ▼
                  ┌─────────────────┐
                  │   SetWZData     │
                  │   (Normalize)   │
                  └────────┬────────┘
                           ▼
                ┌──────────────────────┐
                │   AI Agent Parser    │
                │   (LangChain)        │
                │   - Gemini/OpenAI    │
                │   - Structured Output│
                └──────────┬───────────┘
                           ▼
                ┌──────────────────────┐
                │  SetFinalFields      │
                │  (Map to Schema)     │
                └──────┬───────────────┘
                       │
           ┌───────────┼───────────┐
           ▼           ▼           ▼
    ┌──────────┐ ┌─────────┐ ┌──────────┐
    │  Google  │ │ Notion  │ │ Airtable │
    │  Sheets  │ │Database │ │  Record  │
    └──────────┘ └─────────┘ └──────────┘
📦 Prerequisites
Required Tools

n8n (self-hosted or cloud) - v1.0+ recommended
Node.js - v18+
Google Cloud Project with APIs enabled:

Google Drive API
Google Sheets API
Gmail API (optional)
Google Gemini API (AI/ML)



API Accounts & Keys

Google Cloud Platform account with OAuth2 credentials
OpenAI API Key (optional, for GPT-4 Vision alternative)
Notion Integration Token (for Notion database)
Airtable API Key (for Airtable integration)

n8n Nodes Required
Standard n8n nodes (pre-installed):

n8n-nodes-base.googleDrive
n8n-nodes-base.googleSheets
n8n-nodes-base.gmailTrigger
n8n-nodes-base.extractFromFile
n8n-nodes-base.set
n8n-nodes-base.if
n8n-nodes-base.notion
Community nodes (install separately):
@n8n/n8n-nodes-langchain (AI agent framework)
n8n-nodes-base.airtable
