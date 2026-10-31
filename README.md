# Multilingual Cooperative Governance and Legal Assistance Chatbot

A Flask-based multilingual chatbot for Indian Cooperative Society Governance and Legal Assistance, providing intelligent query resolution, voice support via Sarvam AI, and Gemini-powered legal RAG (Retrieval-Augmented Generation).

---

## 🌟 Key Features

- **Multilingual Support**: Supports Indian languages (Tamil, Telugu, Malayalam, Kannada, Bengali, Marathi, Gujarati, Punjabi, Odia, Assamese, and English).
- **Voice Input & Output**: Speech-to-text (STT) and text-to-speech (TTS) integrated with Sarvam AI API.
- **RAG & Knowledge Base**: SQLite-backed knowledge base with Gemini AI fallback for legal and cooperative queries.
- **Admin Dashboard**: Web interface for managing the knowledge base, viewing user enquiries, and updating cooperative governance data.
- **Responsive Web UI**: Built-in chat interface with voice recording and language switching capabilities.

---

## 🚀 Getting Started

### 1. Prerequisites
- Python 3.10+
- (Optional) Gemini API key for AI-powered responses
- (Optional) Sarvam AI API key for multilingual voice input/output

### 2. Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/Rajasree202006/-Multilingual-Cooperative-Governance-Chatbot.git
cd -Multilingual-Cooperative-Governance-Chatbot
pip install -r requirements.txt
```

### 3. Environment Variables (Optional)

Create a `.env` file in the root directory:

```env
GEMINI_API_KEY=your_gemini_api_key_here
SARVAM_API_KEY=your_sarvam_api_key_here
```

### 4. Running the Application

Initialize the database (if needed) and run the Flask application:

```bash
python app.py
```

The application will start at: `http://localhost:5000`

---

## 📁 Project Structure

```
├── static/              # CSS stylesheets and client JavaScript
│   ├── js/main.js       # Voice and chat interaction scripts
│   └── style.css        # UI styling
├── templates/           # HTML templates for Chat & Admin portal
│   ├── admin.html
│   ├── admin_login.html
│   ├── edit_knowledge.html
│   ├── enquiries.html
│   ├── index.html
│   └── knowledge.html
├── add_languages.py     # Multilingual data import helper
├── app.py               # Main Flask application and API endpoints
├── check_database.py    # Database diagnostic utility
├── check_enquiry_table.py
├── cooperative.db       # SQLite database storing knowledge & enquiries
├── data.json            # Seed knowledge base data
├── database.py          # SQLite database schema and helper functions
├── enquiries.json       # Enquiry storage fallback
├── fix_database.py      # Database repair script
├── migrate_data.py      # Data migration utility
├── rag_engine.py        # Gemini-based RAG engine
├── sarvam_voice.py      # Sarvam AI voice integration
└── test_enquiry.py      # Enquiry testing script
```

---

## 🔒 Admin Access

To access the admin dashboard:
1. Navigate to `http://localhost:5000/admin/login`
2. Enter the admin credentials (default configured in `app.py`)
