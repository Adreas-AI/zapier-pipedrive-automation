# Zapier → Pipedrive Lead Automation

Automation workflow: **Webhook → Zapier → Pipedrive**.

This project demonstrates a Zapier automation that receives lead events via webhook and logs them inside **Pipedrive CRM**.

---

## Automation Flow

Webhook → Zapier → Pipedrive CRM

1. Receive lead event from webhook
2. Find person in Pipedrive (by email)
3. Create person if not found
4. Update person
5. Create a note with campaign + event details
6. Zapier Paths for conditional automation logic

---

## Example Webhook Payload

```json
{
  "name": "Test Lead",
  "email": "testlead@example.com",
  "campaign": "linkedin_outreach",
  "event": "reply - user asked for a meeting"
}
