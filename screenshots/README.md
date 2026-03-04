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
```
Files:

- webhook_payload_example.json
- pipedrive_fields_mapping.json


## Project Structure

```text
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
```

## Automation Screenshots

### Webhook Trigger (Catch Hook)
![Webhook Trigger](./screenshots/webhook%20trigger%20%28catch%20hook%29.png)

### Find Person (Pipedrive)
![Find Person](./screenshots/find%20person%20%28Pipedrive%29.png)

### Create Person (Pipedrive)
![Create Person](./screenshots/create%20person%20%28Pipedrive%29.png)

### Update Person (Pipedrive)
![Update Person](./screenshots/Update%20person%20%28Pipedrive%29.png)

### Create Note (Pipedrive)
![Create Note](./screenshots/create%20note%20%28Pipedrive%29.png)

### Zapier Paths
![Zapier Paths](./screenshots/zapier%20paths.png)

---

## Author
Andreas Andrigiannakis






























