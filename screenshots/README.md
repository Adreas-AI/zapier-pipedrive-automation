# Zapier → Pipedrive Lead Automation

Automation workflow: **Webhook → Zapier → Pipedrive**.

This project demonstrates a simple sales automation where lead events are sent via webhook and automatically logged inside **Pipedrive CRM** using **Zapier**.

The automation:
- receives lead data
- finds or creates the contact
- updates the person
- logs campaign activity
- triggers different actions using Zapier Paths

---

# Automation Flow

Webhook → Zapier → Pipedrive CRM

1. Receive lead event from webhook
2. Search if the person already exists in Pipedrive
3. Create the person if they do not exist
4. Update the person information
5. Create a note with campaign + event details
6. Use Zapier Paths for conditional automation logic

---

# Example Webhook Payload
Example payload sent to the Zapier webhook:

{
"name": "Test Lead",
"email": "testlead@example.com",
"campaign": "linkedin_outreach",
"event": "reply - user asked for a meeting"
}

The repository also contains:

webhook_payload_example.json

pipedrive_fields_mapping.json

These files document the payload structure and how the fields are mapped to Pipedrive.

# Project Structure


.
├── README.md
├── webhook_payload_example.json
├── pipedrive_fields_mapping.json
└── screenshots
├── webhook trigger (catch hook).png
├── find person (Pipedrive).png
├── create person (Pipedrive).png
├── update person (Pipedrive).png
├── create note (Pipedrive).png
└── zapier paths.png

---

# Automation Screenshots

## Webhook Trigger (Catch Hook)

![Webhook Trigger](./screenshots/webhook%20trigger%20%28catch%20hook%29.png)

---

## Find Person in Pipedrive

![Find Person](./screenshots/find%20person%20%28Pipedrive%29.png)

---

## Create Person in Pipedrive

![Create Person](./screenshots/create%20person%20%28Pipedrive%29.png)

---

## Update Person in Pipedrive

![Update Person](./screenshots/update%20person%20%28Pipedrive%29.png)

---

## Create Note in Pipedrive

![Create Note](./screenshots/create%20note%20%28Pipedrive%29.png)

---

## Zapier Paths Logic

![Zapier Paths](./screenshots/zapier%20paths.png)

---

# Technologies Used

- Zapier
- Webhooks
- Pipedrive CRM
- Automation workflows

---


Andreas Andrigiannakis
