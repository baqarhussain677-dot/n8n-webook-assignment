This project is part of my learning journey with n8n and workflow automation. I created a simple workflow that receives POST requests through a webhook and returns a static JSON response. I also tested it using Postman to make sure everything works correctly. The main purpose of this project is to understand how webhooks work and gain practical experience with automation.

Local Setup
1. Install Docker Desktop on your computer.
2. Start Docker Desktop.
3. Run n8n using Docker.
4. Open your browser and visit http://localhost:5678.
5. Start creating and testing your workflow.


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
