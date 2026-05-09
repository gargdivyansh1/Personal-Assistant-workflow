# Personal AI Assistant using n8n + Streamlit

An AI-powered Personal Assistant built using **n8n**, **Streamlit**, **Google Gemini**, and multiple Google productivity integrations.

This assistant can:

- Answer general questions
- Manage Google Calendar events
- Read and send Gmail emails
- Create and manage Google Tasks
- Create and update Notes using Google Docs
- Track expenses using Google Sheets
- Maintain conversation memory

The frontend is built using **Streamlit**, while the backend orchestration and tool automation are handled using **n8n AI Agent workflows**.

---

# 🚀 Features

## ✅ AI Chat Assistant
- Conversational AI interface
- Context-aware responses using memory
- Powered by Google Gemini

## 📅 Calendar Management
- Create events
- Fetch upcoming meetings
- Get details of specific events

## 📧 Gmail Integration
- Read emails
- Summarize inbox
- Send and reply to emails

## 📝 Notes Management
- Create notes in Google Docs
- Append updates to notes
- Read existing notes

## ✅ Task Management
- Create tasks
- Read tasks
- Delete completed tasks

## 💰 Expense Tracking
- Add expenses to Google Sheets
- Fetch expense history
- Perform budget calculations

## 🌐 Web Search
- Uses SerpAPI for Google Search
- Fetches real-time information

---

# 🏗️ Tech Stack

## Frontend
- Streamlit

## Backend Automation
- n8n

## AI Model
- Google Gemini (`gemma-4-26b-a4b-it`)

## Integrations
- Google Calendar API
- Gmail API
- Google Docs API
- Google Tasks API
- Google Sheets API
- SerpAPI

---

# 📂 Project Structure

```bash
personal-ai-assistant/
│
├── app.py                  # Streamlit frontend
├── README.md
├── requirements.txt
├── workflow.json           # n8n workflow export
│
└── assets/
```

---

# ⚙️ Workflow Architecture

```text
Streamlit UI
      │
      ▼
Webhook (n8n)
      │
      ▼
AI Agent (Gemini + Memory)
      │
 ┌────┼────┬────┬────┬────┐
 ▼    ▼    ▼    ▼    ▼
Search Gmail Calendar Tasks Notes Expenses
```

---

# 🧠 AI Agent Capabilities

The AI agent behaves like an executive personal assistant and is capable of:

- Intent understanding
- Tool selection
- Task execution
- Memory retention
- Safe operation handling

The agent dynamically chooses tools based on user requests.

---

# 📸 Streamlit Frontend

The frontend provides:

- Chat interface
- Session-based memory
- Real-time assistant responses
- Clean conversational UI

Example:

```python
user_message = st.chat_input()

response = requests.post(
    "http://localhost:5678/webhook/your-webhook-id",
    json={"message": user_message}
)
```

---

# 🔧 Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/yourusername/personal-ai-assistant.git

cd personal-ai-assistant
```

---

## 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3️⃣ Start n8n

```bash
n8n start
```

n8n will run on:

```bash
http://localhost:5678
```

---

## 4️⃣ Import Workflow

Import the exported workflow JSON into n8n.

Workflow File:

```bash
workflow.json
```

---

## 5️⃣ Configure Credentials

Inside n8n configure:

- Google Gemini API
- Google Calendar OAuth
- Gmail OAuth
- Google Docs OAuth
- Google Sheets OAuth
- Google Tasks OAuth
- SerpAPI

---

## 6️⃣ Run Streamlit App

```bash
streamlit run app.py
```

---

# 🔑 Required APIs

## Google APIs
Enable:

- Gmail API
- Google Calendar API
- Google Docs API
- Google Sheets API
- Google Tasks API

Google Cloud Console:

https://console.cloud.google.com

---

## SerpAPI

Get API key from:

https://serpapi.com

---

## Google Gemini API

Get API key from:

https://aistudio.google.com

---

# 🧩 n8n Nodes Used

## Core Nodes
- Webhook
- AI Agent
- Respond to Webhook
- Memory Buffer Window

## AI Model
- Google Gemini Chat Model

## Productivity Tools
- Google Calendar Tool
- Gmail Tool
- Google Docs Tool
- Google Tasks Tool
- Google Sheets Tool

## Utilities
- Calculator
- SerpAPI Search

---

# 💬 Example Prompts

## Calendar
```text
Schedule a meeting tomorrow at 5 PM
```

## Gmail
```text
Summarize my unread emails
```

## Notes
```text
Create notes for my ML revision
```

## Tasks
```text
Add task to complete DSA assignment
```

## Expenses
```text
Add ₹500 expense for groceries
```

---

# 🔒 Safety Features

- Prevents hallucinated actions
- Requires explicit deletion requests
- Structured tool-based execution
- Minimal unnecessary verbosity

---

# 📌 Future Improvements

- Voice assistant support
- WhatsApp integration
- Telegram bot support
- Multi-user authentication
- Vector database memory
- RAG document retrieval
- Mobile app support
- Docker deployment

---

# 🛠️ requirements.txt

```txt
streamlit
requests
google-generativeai
python-dotenv
```

---

# 👨‍💻 Author

## Divyansh Garg

- AI/ML Developer
- Full Stack Developer
- B.Tech CSE + Computer Vision

### GitHub
https://github.com/gargdivyansh1

### LinkedIn
https://www.linkedin.com/in/divyansh-garg515/

---

# ⭐ Conclusion

This project demonstrates how modern AI agents can be combined with workflow automation to build a powerful real-world personal assistant capable of managing productivity tasks autonomously using natural language.