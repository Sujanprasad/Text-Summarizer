# 🧠 Text Summarizer

A lightweight AI-powered **Text Summarizer Web App** that extracts only the **most important meaning** from long text instead of rewriting the entire content.

This project uses a **clean frontend (HTML + Bootstrap)** and a **serverless AI backend powered by n8n Webhooks and OpenAI**.

---

## 🚀 Live Demo
👉 *(Add your hosted link here once deployed)*

---

## ✨ Features

- 📌 Extracts **Main Topic** and **Important Topics**
- 🧠 Focuses only on **high-importance meaning**
- 🎯 Avoids unnecessary summarization and filler
- ⚡ Fast response using n8n Webhooks
- 🎨 Modern dark UI with Bootstrap
- 🔢 Character limit with live counter (1000 chars)
- 🌐 Fully frontend-based (no backend hosting needed)

---

## 🛠️ Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript (Vanilla)
- Bootstrap 5

### Backend / AI
- n8n (Cloud)
- Webhook Trigger
- LangChain AI Agent
- OpenAI (GPT-4.1-mini)

---

## 🧩 Project Architecture

User Input (Browser)
↓
HTML + JavaScript UI
↓
n8n Webhook (POST)
↓
AI Agent (LangChain)
↓
OpenAI Model
↓
Structured Response
↓
Rendered Output (Main Topic + Important Topics)

yaml
Copy code

---

## 📂 Project Structure

├── index.html # Frontend UI
├── README.md # Project documentation
└── n8n-workflow.json # Text Summarizer API workflow

markdown
Copy code

---

## ⚙️ How It Works

1. User pastes text (up to 1000 characters)
2. Frontend sends text to an **n8n Webhook**
3. AI Agent analyzes content using strict instructions:
   - Extract only core topics
   - Avoid minor details
   - Keep meaning intact
4. Response is returned in a structured format
5. UI displays:
   - **Main Topic**
   - **Important Topics with explanations**

---

## 🔌 n8n Workflow Setup

1. Import `Text Summarizer API.json` into n8n
2. Ensure these nodes are connected:
   - Webhook
   - AI Agent (LangChain)
   - OpenAI Chat Model
   - Respond to Webhook
3. Enable CORS in the response node
4. Copy the webhook URL and update it in `index.html`

```js
const WEBHOOK_URL = "YOUR_N8N_WEBHOOK_URL";
## ▶️ Running Locally
Since this is a pure frontend app:

bash
Copy code
# Option 1: Open directly
Open index.html in browser

# Option 2: Using VS Code Live Server
Right click → Open with Live Server
🧪 Example Output
Main Topic

Clearly identifies the overall subject of the text

Important Topics

Lists only high-impact points with concise explanations

🔐 Security Notes
Do NOT expose your OpenAI API key in frontend code

All AI processing happens inside n8n

Frontend only communicates via webhook

🌱 Future Improvements
File upload support (PDF / DOCX)

Summary length controls

Topic-based highlighting

User authentication

Save history of summaries

👤 Author
Sujan Panda
Full-Stack Python Developer
AI • Automation • Web Apps

