# AI QA Bug Triage Automation

An AI-powered QA bug triage workflow built with n8n.

## Overview

This project demonstrates an automated QA workflow that receives a bug report through a webhook, normalizes the input, performs bug triage, checks for duplicates, and routes the bug accordingly.

## Workflow

Postman / Bug Report
        ↓
n8n Webhook
        ↓
Edit Fields
        ↓
AI Triage
        ↓
Duplicate Detection
        ↓
Is Duplicate?
      ↙       ↘
   YES          NO
    ↓            ↓
Duplicate     Prepare Bug
Response          ↓
              Jira Creation
              ↓
             Response

## Current MVP

The current version demonstrates:

- Webhook-based bug ingestion
- Bug data normalization
- Structured QA triage
- Duplicate bug detection
- Duplicate/new bug branching
- Mock Jira ticket creation
- JSON response to the caller

## Technology

- n8n
- AI / LLM
- Webhooks
- Postman
- Jira integration concept
- QA Automation

## Current Status

This is an MVP/prototype.

The AI processing and Jira creation are currently mocked in the main execution path. The workflow also contains the configured AI Agent structure for future LLM integration.

## Future Enhancements

- Connect a real LLM
- Integrate Jira API
- Improve semantic duplicate detection
- Add Playwright test failure ingestion
- Analyze screenshots and stack traces
- Add automated root-cause analysis
- Add notifications through Slack/Teams
- Add historical bug memory/RAG