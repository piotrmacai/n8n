# n8n Website Complete SEO Audit

A comprehensive n8n workflow for running a full-scale SEO, AEO, and technical website audit, enriched with AI agents and optional Google Analytics insights.

![SEO Audit Workflow](seoaudit.jpeg)

## Workflow Overview

This workflow is structured as a modular, multi-agent SEO audit pipeline:

1. **Trigger & Setup**
   - Webhook or landing page URL input
   - Automatic Google Drive folder creation
   - Initialization via AI Agent

2. **Technical HTML Audit**
   - Website scraping
   - Technical HTML and on-page SEO analysis
   - AI-driven technical findings and recommendations

3. **SEO Content & Metadata Analysis**
   - **Meta Data Agent** – titles, meta descriptions, structure
   - **Content Agent** – on-page content quality and optimization
   - **AEO / Keyword Audit Agent** – keyword coverage and answer-engine readiness

4. **Report Generation**
   - JavaScript processing and formatting
   - Individual audit files generated in Google Drive
   - Merging of all audit sections into a single dataset

5. **Summary Agent**
   - AI-generated executive summary
   - Clean, client-ready final output
   - Conditional logic for delivery or further processing

6. **Optional: Google Analytics Agent**
   - Fetches GA data
   - Adds traffic and performance context to the audit

## Tech Stack

- **n8n**
- **AI Agents (LLM / Google Gemini)**
- **Google Drive**
- **JavaScript (Code nodes)**
- **Webhooks & HTTP Scraping**
- **Google Analytics (optional)**

## Use Cases

- Full technical SEO audits  
- Content, metadata, and keyword analysis  
- AEO (Answer Engine Optimization) readiness checks  
- Agency-ready, scalable AI audit system  
- Foundation for SEO audit SaaS products  
