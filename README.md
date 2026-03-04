# Zapier → Pipedrive Lead Automation

Automation workflow: **Webhook → Zapier → Pipedrive**.

This project demonstrates a Zapier automation that receives lead events via webhook and logs them inside **Pipedrive CRM**.

---

## Tools
- Zapier (Webhooks + Paths)
- Pipedrive CRM
- JSON

---

## Automation Flow
1. Webhook receives JSON payload (`name`, `email`, `campaign`, `event`)
2. Find Person in Pipedrive (by email)
3. Create Person (if not found)
4. Update Person
5. Create Note (logs `campaign` + `event`)
6. Zapier Paths:
   - If event contains `reply` → Create Activity (Meeting)
   - If event contains `open` → Create Activity (Email Opened)

---

## Example Webhook Payload

```json
{
  "name": "Test Lead",
  "email": "testlead@example.com",
  "campaign": "linkedin_outreach",
  "event": "reply - user asked for a meeting"
}
```
Files:

webhook_payload_example.json

pipedrive_fields_mapping.json

Project Structure
.
├── README.md
├── webhook_payload_example.json
├── pipedrive_fields_mapping.json
└── screenshots/
    ├── webhook trigger (catch hook).png
    ├── find person (Pipedrive).png
    ├── create person (Pipedrive).png
    ├── Update person (Pipedrive).png
    ├── create note (Pipedrive).png
    └── zapier paths.png


Automation Screenshots
Webhook Trigger (Catch Hook)

Find Person (Pipedrive)

Create Person (Pipedrive)

Update Person (Pipedrive)

Create Note (Pipedrive)

Zapier Paths

Author

Andreas Andrigiannakis

































  "event": "reply - user asked for a meeting"
}
