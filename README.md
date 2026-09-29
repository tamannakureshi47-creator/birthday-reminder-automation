# 🎂 n8n Birthday Reminder Automation

An automated birthday reminder workflow built with n8n, Google Sheets, an AI Agent, OpenAI Chat Model, and WhatsApp.

This workflow reads birthday records from a Google Sheet, processes the data, generates a personalized birthday message using an AI Agent, sends the message through WhatsApp, and updates the spreadsheet.

## ✨ Features

- Scheduled automation using n8n Schedule Trigger
- Google Sheets integration
- JavaScript data processing
- AI-generated personalized birthday messages
- OpenAI Chat Model integration
- WhatsApp message delivery
- Google Sheets row update after processing
- Low-code automation workflow

## 🧩 Workflow

Schedule Trigger
        ↓
Get Row(s) in Sheet
        ↓
Code in JavaScript
        ↓
AI Agent
        ↓
OpenAI Chat Model
        ↓
Send WhatsApp Message
        ↓
Append or Update Row in Sheet

## 🛠️ Technologies Used

- n8n
- Google Sheets
- JavaScript
- OpenAI
- AI Agent
- WhatsApp

## 📋 Requirements

Before using this workflow, you need:

- An n8n Cloud or self-hosted instance
- A Google account
- A Google Sheet containing birthday records
- Google Sheets credentials configured in n8n
- OpenAI API credentials
- WhatsApp integration and valid credentials

## 📊 Google Sheet Example

Your Google Sheet can contain columns like:

| Name | Birthday | Phone | Last Reminder Sent |
|------|----------|-------|---------------------|
| John | 1998-09-29 | +XXXXXXXXXX | |

You can modify the column names according to your workflow.

## 🚀 Setup

### 1. Create the Google Sheet

Create a spreadsheet containing the birthday information of your contacts.

Make sure the birthday and phone number fields are stored in a format that your workflow can process correctly.

### 2. Import the n8n Workflow

Export the workflow from n8n as a JSON file.

Then import the JSON workflow into your n8n instance.

### 3. Configure Google Sheets

Connect your Google account to the Google Sheets nodes.

Select:

- Spreadsheet
- Sheet
- Required columns

### 4. Configure JavaScript

The JavaScript node processes the spreadsheet data and prepares the information required by the AI Agent.

Make sure the field names in the JavaScript code match your Google Sheet columns.

### 5. Configure AI Agent

Connect the AI Agent with the OpenAI Chat Model.

The AI Agent generates a personalized birthday message based on the birthday information.

Example message:

"Happy Birthday, John! 🎉🎂 Wishing you a wonderful day filled with happiness, success, and lots of memorable moments. Have an amazing birthday!"

### 6. Configure WhatsApp

Connect your WhatsApp integration and configure the required credentials.

Map:

- Recipient phone number
- Generated birthday message

Always test the WhatsApp node with a test number before enabling the complete automation.

### 7. Update Google Sheet

The final Google Sheets node updates the processed row.

This can be used to store information such as:

- Reminder sent
- Date sent
- Message status

## ⚙️ Automation Flow

The workflow runs automatically according to the configured Schedule Trigger.

When the workflow runs:

1. The Schedule Trigger starts the workflow.
2. Birthday records are retrieved from Google Sheets.
3. JavaScript processes the records.
4. The AI Agent generates a personalized message.
5. WhatsApp sends the message.
6. Google Sheets is updated after processing.

## 🔐 Security

Do not commit sensitive information to GitHub.

Never upload:

- API keys
- Access tokens
- WhatsApp credentials
- Google credentials
- Private phone numbers
- Personal customer information
- Environment variables containing secrets

Before uploading the n8n workflow JSON, review the exported file and remove any sensitive credentials or private information.

## 🧪 Testing Checklist

Before publishing the workflow, verify:

- [ ] Schedule Trigger works correctly
- [ ] Google Sheet data is retrieved correctly
- [ ] Birthday filtering works correctly
- [ ] AI Agent generates the expected message
- [ ] WhatsApp sends the message successfully
- [ ] Correct spreadsheet row is updated
- [ ] Duplicate birthday messages are prevented
- [ ] Invalid phone numbers are handled properly

## 💡 Future Improvements

Possible improvements include:

- Telegram birthday notifications
- Email birthday reminders
- Multiple WhatsApp message templates
- Birthday reminder dashboard
- Error notification system
- Message delivery status tracking
- Duplicate message prevention
- Monthly birthday report
- Admin notification when a birthday message is sent

## 📁 Repository Structure

n8n-birthday-reminder-automation/
│
├── README.md
├── workflow.json
│
└── screenshots/
    └── workflow.png

## 🤝 Contributing

Suggestions and improvements are welcome.

If you find an issue or have an idea for improving the workflow, feel free to create an issue or submit a pull request.

<img width="2676" height="977" alt="screencapture-tamanna2-app-n8n-cloud-workflow-IUhwh5L67lcCJxrI-2026-09-29-13_04_46" src="https://github.com/user-attachments/assets/a36ebc82-00a1-4a03-953e-890c2cf0a6c3" />

