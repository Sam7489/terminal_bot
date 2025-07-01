# 🧠 Terminal AI ChatBot — Powered by Groq

A minimal and fast terminal-based AI chatbot built with Python and Groq’s LLaMA 3 model.  
This tool allows you to interact with a personalized AI assistant directly from your Linux terminal — optimized for concise answers, command-line usage, and session logging.

---

## 🚀 Features

- 💬 Ask natural language queries from the terminal
- 🧠 Custom system prompt to personalize the bot's behavior
- 🧾 Maintains conversation logs in `chatlog.json`
- 📦 Use `-new` to archive current session into `history.json`
- 🔐 Keeps your API keys secure via `.env` file
- 💡 Ideal for pentesters, coders, and terminal geeks

---

## 📸 Demo

```bash
$ bot "How to scan ports with nmap?"
🤖 CyberBuddy:
```bash
nmap -sV -T4 <target-ip>
$ bot -new
📦 Archived current chatlog to history.json and started a new session.



## 🛠️ Installation

### 1. Clone the repo

```bash
git clone https://github.com/Sam7489/terminal_bot.git
cd terminal_bot
2. Create a virtual environment

python3 -m venv venv
source venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

4. Create a .env file

cp .env.example .env

Then open .env and fill in your details:

GroqAPIKey=your-groq-api-key-here
Username=Sam
Assistantname=CyberBuddy


🧠 Usage
✅ Chat with the bot

bot "your question here"
Example:

bot "Give me a curl command to send a POST request"

🔁 Start a new session
This will archive the current chatlog.json into history.json:

bot -new

🆘 Help

bot -h

📁 Project Structure

terminal_bot/
├── bot.py              # Main chatbot logic
├── .env                # (Not included in repo) — your API keys
├── .env.example        # Template for environment variables
├── chatlog.json        # Stores ongoing conversation
├── history.json        # Archives past sessions when -new is used
├── requirements.txt    # Python dependencies
└── README.md           # You're here!
