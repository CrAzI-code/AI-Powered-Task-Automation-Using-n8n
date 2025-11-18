# AI-Powered-Task-Automation-Using-n8n
This project is an AI-assisted automation workflow built with n8n that allows a user to create structured tasks or events using a simple chat message.  When a user sends a text command (e.g., “Add meeting with Musa tomorrow by 2pm, high priority”), the workflow does the following automatically:

Features

 Accepts free-text task/event details through an n8n Trigger
 AI parses the message into structured fields:
  • Task / Event Name
  • Description
  • Due Date
  • Priority

 Adds the event to Google Calendar
 Logs the task into Google Sheets under columns:
 Fully automated — no manual entry required
 Works with any chat trigger (Telegram, WhatsApp, n8n AI Chat, Webhook, etc.)

#How It Works (Simple Explanation)

1. User Sends a Chat Message
   Example: “Create a task: Finish cybersecurity report tomorrow morning, priority high.”

2. AI Node Parses the Text
   The AI extracts structured info like:

  Title: Cybersecurity Report

  Description: Finish the cybersecurity report

  Due Date: Tomorrow morning

  Priority: High

3. Google Calendar Node Creates the Event
   Using the parsed data, n8n automatically creates the event.

4. Google Sheets Node Logs the Entry
The automation inserts a new row into your prepared spreadsheet.


#Workflow Structure

The workflow includes these nodes:

1. Trigger Node → (Telegram/AI Chat/Webhook)

2. AI Parser Node → Extracts task fields

3. AI Chat model

4. Simple Memory model

5. Google Sheets Node → Appends row
  
6. Google Sheets Node → Get row

7. Google Sheets Node → Update row

8. Google Calendar Node → Creates event

9. Google Calendar Node → Get Many

(Optional) Formatter Node → Cleans dates, text

(Optional) Response Node → Sends confirmation back to user

<img width="1894" height="947" alt="Screenshot 2025-11-18 033932" src="https://github.com/user-attachments/assets/8f86e430-69c7-4f57-9380-0e924ed5d833" />



