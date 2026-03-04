# Zapier → Pipedrive Lead Automation

This project demonstrates a **CRM automation workflow** built with **Zapier Webhooks and Pipedrive**.

The automation captures lead events via webhook and updates the CRM with notes and activities depending on the event type.

---

# Tools Used

- Zapier (Webhooks + Paths)
- Pipedrive CRM
- JSON payloads
- Webhook testing (ReqBin / Postman)

---

# Automation Workflow

Webhook → Zapier → Pipedrive

1. Zapier receives lead event via **Webhook (Catch Hook)**
2. Zapier **Finds Person in Pipedrive** using email
3. If the person does not exist → **Create Person**
4. Update the person record
5. Create a **Note** logging the event and campaign
6. Use **Zapier Paths** for conditional logic

### Path A
If event contains **reply**

→ Create Activity: **Meeting**

### Path B
If event contains **open**

→ Create Activity: **Email Opened**

---

# Example Webhook Payload

```json
{
  "name": "Test Lead",
  "email": "testlead@example.com",
  "campaign": "linkedin_outreach",
  "event": "reply - user asked for a meeting"
}
