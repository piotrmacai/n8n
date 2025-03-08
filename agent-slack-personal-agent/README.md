# Slack Personal AI Assistant (n8n)

This Slack Personal AI Assistant is an n8n workflow designed to enhance Slack communication by integrating AI-powered automation. It supports both text and voice input, utilizes OpenAI for transcription and responses, and connects with various tools like Gmail, Google Calendar, and Notion for seamless workflow automation.


# Features

🗣 Voice & Text Input Support: Users can send voice recordings or text messages to Slack.

🤖 AI-Powered Responses: Utilizes OpenAI models for transcription and intelligent replies.

📅 Google Calendar Integration: Schedule and manage events directly from Slack.

📧 Gmail Automation: Retrieve emails and send automated replies.

🧠 Custom Knowledge Base: Stores context and retrieves relevant information using Notion or other database tools.

🔄 Memory & Context Handling: Uses window buffer memory to keep track of conversations.


# Workflow Diagram

The assistant's workflow consists of the following steps:

Slack Trigger: Captures user messages (text/voice) from a Slack channel.

Switch Node: Routes input based on type (voice or text).

OpenAI API: Transcribes voice messages and processes text inputs.

AI Agent (Tools Agent): Processes the query and determines the required action.

External Integrations:

Google Calendar: Retrieves or schedules events.

Gmail: Fetches emails or sends responses.

Notion/CRM Database: Retrieves stored knowledge.

Slack Response: Posts the processed output back to Slack.



# Prerequisites

n8n installed (Self-hosted or Cloud version)

Slack API Token (for bot integration)

OpenAI API Key (for AI processing)

Google API Credentials (for Calendar and Gmail access)

Notion API Key (if using a knowledge base)
