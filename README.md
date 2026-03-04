# Zapier → Pipedrive Lead Automation

This project demonstrates a CRM automation workflow that captures leads 
via webhook and automatically creates contacts in Pipedrive using Zapier.

## Tools
- Zapier
- Webhooks
- Pipedrive CRM
- JSON

## Workflow

1. A lead submits data (form / outreach tool)
2. A webhook sends the lead data in JSON format
3. Zapier receives the webhook
4. Zapier maps the fields
5. Pipedrive creates a new contact or lead

## Example Payload

See: webhook_payload_example.json

## Use Cases

- Lead generation automation
- CRM integrations

- ## Automation Flow

Webhook → Zapier → Pipedrive CRM

Lead event received via webhook  
↓  
Find Person in Pipedrive (by email)  
↓  
Create Person (if not exists)  
↓  
Update Person  
↓  
Create Note (log event)  
↓  
Zapier Paths  

Path A  
If event contains **reply**  
→ Create Activity: Meeting  

Path B  
If event contains **open**  
→ Create Activity: Email Opened
- Marketing automation

## Screenshots

(See folder: /screenshots)

- Sales pipeline automation
