# Multilingual Cooperative Governance and Legal Assistance Chatbot

[![Live Demo](https://img.shields.io/badge/Live_Website-Online-success?style=for-the-badge&logo=github)](https://rajasree202006.github.io/-Multilingual-Cooperative-Governance-Chatbot/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

An intelligent, accessible, and multilingual AI assistant for Indian Cooperative Society Governance, Primary Agricultural Credit Societies (PACS), and member legal assistance.

---

## 🌐 Live Website Access

You can open and interact with the live AI project immediately in any web browser (no local setup required):

👉 **[https://rajasree202006.github.io/-Multilingual-Cooperative-Governance-Chatbot/](https://rajasree202006.github.io/-Multilingual-Cooperative-Governance-Chatbot/)**

---

## 🌟 Key Features

- **Multilingual Support (12 Indian Languages)**: Full native Q&A in English, Tamil (தமிழ்), Hindi (हिन्दी), Telugu (తెలుగు), Malayalam (മലയാളം), Kannada (ಕನ್ನಡ), Bengali (বাংলা), Marathi (मराठी), Gujarati (ગુજરાતી), Punjabi (ਪੰਜਾਬੀ), Odia (ଓଡ଼ିଆ), and Assamese (অসমীয়া).
- **Voice AI Interface**:
  - 🎤 **Voice Input (Speech-to-Text)**: Speak directly into the microphone with automated regional language recognition.
  - 🔊 **Voice Output (Text-to-Speech)**: High-clarity native speech synthesis reading answers aloud.
- **Instant Hybrid RAG Engine**:
  - Over **180+ verified cooperative legal articles** covering PACS, KCC short-term crop loans (4% effective interest rate), PMFBY insurance, member rights, by-laws, audits, and board election procedures.
  - Client-side keyword scoring algorithm guarantees zero cold-start delay and offline availability.
- **Gemini 1.5 Legal AI Mode**:
  - Built-in option to connect Google Gemini 1.5 Flash API for free-form advisory on complex cooperative legal scenarios.
- **Member Grievance & Enquiry Management**:
  - Submit official member enquiries with auto-generated tracking codes (e.g., `ENQ-2026-XXXX`).
  - Real-time Enquiry Status Tracker showing administrative review progression.
  - Local administrator drawer for reviewing registered cases.

---

## 🚀 Deployment Options

### 1. GitHub Pages (Static / Serverless Web App)
The frontend (`index.html` + `data.js`) runs natively on **GitHub Pages**:
- URL: `https://rajasree202006.github.io/-Multilingual-Cooperative-Governance-Chatbot/`
- Automated continuous deployment via `.github/workflows/deploy-pages.yml`.

### 2. Full Flask Backend on Render.com (1-Click Cloud Hosting)
For running the complete Python backend (`app.py`, SQLite `cooperative.db`, and Sarvam AI backend):
1. Sign in to [Render.com](https://render.com).
2. Click **New +** -> **Web Service** -> Connect `https://github.com/Rajasree202006/-Multilingual-Cooperative-Governance-Chatbot`.
3. Render automatically detects `render.yaml` and `Procfile`.
4. Click **Deploy Web Service** to get a dedicated `https://<your-app>.onrender.com` URL.

---

## 💻 Local Development Setup

```bash
# 1. Clone the repository
git clone https://github.com/Rajasree202006/-Multilingual-Cooperative-Governance-Chatbot.git
cd -Multilingual-Cooperative-Governance-Chatbot

# 2. Install dependencies
pip install -r requirements.txt

# 3. (Optional) Configure environment variables in a .env file
# SARVAM_API_KEY=your_key_here
# GEMINI_API_KEY=your_key_here

# 4. Run the Flask application
python app.py
```

The local application will launch at: `http://localhost:5000`  
Administrator portal: `http://localhost:5000/admin/login`

---

## 📁 Repository Structure

```
├── .github/workflows/   # Automated GitHub Pages CI/CD workflow
├── static/              # CSS stylesheets and client JavaScript
├── templates/           # Flask HTML templates
├── .gitignore           # Git ignore rules
├── Procfile             # Gunicorn deployment config for cloud web services
├── README.md            # Project documentation and live link
├── app.py               # Flask backend API and route controllers
├── cooperative.db       # SQLite cooperative database
├── data.js              # Knowledge base bundle for zero-latency static web hosting
├── data.json            # Structured legal Q&A dataset
├── database.py          # SQLite schema and query functions
├── index.html           # Universal frontend application
├── render.yaml          # Render.com infrastructure blueprint
├── requirements.txt     # Python project dependencies
├── vercel.json          # Vercel serverless configuration
└── sarvam_voice.py      # Sarvam AI voice integration module
```
