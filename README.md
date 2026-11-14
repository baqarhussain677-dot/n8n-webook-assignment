This project is part of my learning journey with n8n and workflow automation. I created a simple workflow that receives POST requests through a webhook and returns a static JSON response. I also tested it using Postman to make sure everything works correctly. The main purpose of this project is to understand how webhooks work and gain practical experience with automation.

Local Setup Instructions

Install Docker Desktop on your computer.

Open Docker Desktop and make sure it is running.

Open PowerShell.

Run the n8n Docker container.

Open your browser and visit http://localhost:5678.

Start creating and testing your webhook workflow.


## Webhook URL and Testing

### Public Webhook URL
The webhook is exposed to the internet using ngrok.

Public URL: `YOUR_NGROK_URL/webhook/YOUR_WEBHOOK_PATH`

Replace the URL above with your actual ngrok webhook URL.

### How to Test
You can test the webhook using Postman or curl.

**Method:** POST

**Body (JSON):**
```json
{
  "name": "Mohsin",
  "message": "Testing my n8n webhook"
}
```

**Using curl:**
```bash
curl -X POST "YOUR_NGROK_URL/webhook/YOUR_WEBHOOK_PATH" \
-H "Content-Type: application/json" \
-d "{\"name\":\"Mohsin\",\"message\":\"Testing my n8n webhook\"}"
```

**Expected Response:**
```json
{
  "success": true,
  "message": "Webhook received successfully"
}
```
