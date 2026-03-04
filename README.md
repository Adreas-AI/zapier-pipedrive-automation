# Zapier → Pipedrive Lead Automation

Automation workflow: **Webhook → Zapier → Pipedrive**  
It captures lead events via webhook and updates Pipedrive with a note + activities using conditional Paths.

## Tools
- Zapier (Webhooks + Paths)
- Pipedrive CRM
- JSON

## Workflow
1. Webhook receives JSON payload (`name`, `email`, `campaign`, `event`)
2. Find Person in Pipedrive (by email)
3. Create Person (if not found)
4. Update Person
5. Create Note (logs `campaign` + `event`)
6. Zapier Paths:
   - **If event contains `reply`** → Create Activity (Meeting)
   - **If event contains `open`** → Create Activity (Email Opened)

## Example Payload (ReqBin / Postman)
```json
{
  "name": "Test Lead",
  "email": "testlead@example.com",
  "campaign": "linkedin_outreach",
  "event": "reply - user asked for a meeting"
}

## Screenshots

### Webhook Trigger (Catch Hook)
![Webhook Trigger](screenshots/webhook%20trigger%20(catch%20hook).png)

### Find Person (Pipedrive)
![Find Person](screenshots/find%20person%20(Pipedrive).png)

### Create Person (Pipedrive)
![Create Person](screenshots/create%20person%20(Pipedrive).png)

### Update Person (Pipedrive)
![Update Person](screenshots/Update%20person%20(Pipedrive).png)

### Create Note (Pipedrive)
![Create Note](screenshots/create%20note%20(Pipedrive).png)

### Zapier Paths
![Zapier Paths](screenshots/zapier%20paths.png)
