# 🤖 AI Order Processing Pipeline

An AI-powered **n8n workflow** that automates the processing of new customer orders by monitoring Airtable, generating professional order summaries with OpenAI, notifying the operations team through Gmail, and updating order statuses automatically.

---

## Overview

This workflow eliminates manual order notification by automatically:

- Monitoring Airtable for new customer orders
- Updating the order status to **Processing**
- Generating a professional internal order summary using OpenAI
- Sending an email notification to the Operations Team
- Updating the order status to **Shipped** on success
- Updating the order status to **Error** if the notification fails

The workflow is designed to demonstrate practical AI automation for internal business operations.

---

## Workflow

```text
Schedule Trigger
        │
        ▼
Find Pending Orders
        │
        ▼
Mark as Processing
        │
        ▼
Generate AI Order Summary
        │
        ▼
Notify Operations Team
     ┌──┴───────────┐
     ▼              ▼
Success          Failure
     │              │
     ▼              ▼
Mark Shipped   Mark as Error
```

---

## Features

- ⏰ Automatic scheduled polling
- 📋 Airtable order management
- 🤖 AI-generated order summaries using OpenAI
- 📧 Automated Gmail notifications
- ✅ Automatic status updates
- ⚠️ Built-in error handling

---

## Technologies Used

- n8n
- OpenAI GPT-4o Mini
- Airtable
- Gmail API

---

## Setup

1. Import the workflow into n8n.
2. Create the following credentials:
   - Airtable Account
   - OpenAI Account
   - Gmail Account
3. Connect your Airtable Base and Table.
4. Replace the placeholder recipient email.
5. Activate the workflow.

---

## Repository Structure

```
.
├── workflows/
│   └── ai-order-processing-pipeline.json
├── LICENSE
└── README.md
```

---

## Future Improvements

Planned enhancements include:

- Batch email notifications
- Slack / Microsoft Teams integration
- Order prioritization
- PDF invoice generation
- Multi-user approval workflows
- Analytics dashboard

---

## License

This project is licensed under the MIT License.
