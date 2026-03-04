# Zapier → Pipedrive Automation (Webhook → CRM)

Simple Zapier automation that receives lead events via webhook and logs them into **Pipedrive**.

## What it does
- Receives a webhook payload (`name`, `email`, `campaign`, `event`)
- Finds or creates a Person in Pipedrive (by email)
- Updates the Person
- Creates a Note with campaign + event details
- Uses Zapier Paths for conditional logic (e.g. reply/open)

## Files
- `webhook_payload_example.json` — sample incoming webhook payload
- `pipedrive_fields_mapping.json` — field mapping / notes about the Zap setup

## Screenshots
Screenshots of the Zap steps are available in the `screenshots/` folder:
- `screenshots/` (contains PNGs + an optional README with visuals)

## Author
Andreas Andrigiannakis
