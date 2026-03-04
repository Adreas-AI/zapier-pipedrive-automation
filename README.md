# Zapier → Pipedrive Lead Automation

This project demonstrates a **Zapier automation workflow** that captures lead events via a webhook and automatically creates or updates contacts inside **Pipedrive CRM**.

The automation also logs campaign activity and uses **Zapier Paths** to trigger different actions depending on the event type.

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

```json
{
"name": "Test Lead",
"email": "testlead@example.com",

See full example here:

webhook_payload_example.json

Field Mapping

The mapping between webhook data and Pipedrive fields is documented in:

pipedrive_fields_mapping.json

Example logic:

Webhook Field	Pipedrive Field
name	person.name
email	person.email
campaign	note content
event	note content

Example note template:

Campaign: {{campaign}} | Event: {{event}}

How to Test the Webhook

Copy the Zapier webhook URL and send a request like this:

curl -X POST "PASTE_ZAPIER_WEBHOOK_URL_HERE" \
-H "Content-Type: application/json" \
-d '{
"name": "Test Lead",
"email": "testlead@example.com",
"campaign": "linkedin_outreach",
"event": "reply - user asked for a meeting"
}'

Then test the Zap inside Zapier and verify the data inside Pipedrive.

Project Structure
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

Automation Screenshots
Webhook Trigger (Catch Hook)

Find Person in Pipedrive

Create Person in Pipedrive

Update Person in Pipedrive

Create Note in Pipedrive

Zapier Paths Logic

Technologies Used

Zapier

Webhooks

Pipedrive CRM

API-based automation

Conditional workflow logic (Zapier Paths)

Use Case

This automation can be used for:

Outbound sales campaigns

Lead tracking

Cold outreach monitoring

CRM activity logging

Automated sales workflows
"campaign": "linkedin_outreach",
"event": "reply - user asked for a meeting"
}
