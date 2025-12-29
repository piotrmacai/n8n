# 360MarketingReports (n8n Workflow)

It's complete marketing reports system - n8n workflow that collects weekly marketing data from Google Ads, Google Analytics, and Meta Ads, then saves a unified report to Google Drive - with conversational AI Agent working with reports data.

![Marketing Reports](marketingreports.jpeg)

## 🔧 What It Does
- Pulls data from:
  - Google Analytics
  - Google Ads
  - Meta (Facebook) Ads
- Combines everything into one weekly report
- Stores the report in Google Drive
- Can be triggered by webhook or on a schedule

## 📦 Workflow Structure
- **Trigger** → starts the workflow
- **Google Analytics Subworkflow**
- **Google Ads Subworkflow**
- **Meta Ads (FB Analytics)**
- **Report generation + Google Drive upload**

## 🔐 Required Access
- Google Analytics API  
- Google Ads API  
- Facebook Business Manager  
- Google Drive (for report storage)
