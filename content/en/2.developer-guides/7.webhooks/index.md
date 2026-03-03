---
title: Overview
description: Receive real-time updates about messages, contacts, conversations, and tickets.
icon: i-lucide-webhook
---

Webhooks allow you to receive real-time `POST` notifications directly to your server when specific events occur in Digishare.

## 1. Setup

::steps
### Set Webhook URL
Configure your endpoint URL in your Digishare application settings.

### Listen for Events
Your server must be ready to receive `POST` requests with a JSON payload.

### Acknowledge Receipt
Your endpoint **must** respond with an HTTP `200 OK` status code to confirm receipt.
::

::warning
If your server does not respond with `200 OK`, Digishare will attempt to resend the notification according to a retry policy before temporarily disabling the webhook.
::



::tip
For updates (`updated`), the payload includes a `changes` object showing only the modified fields and their new values.
::
