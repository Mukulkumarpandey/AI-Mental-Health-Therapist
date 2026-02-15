🧠 AI Mental Health Therapist

An AI-powered Mental Health Support System built using:

⚡ FastAPI (Backend API)

🎨 Streamlit (Frontend UI)

🤖 LangChain + LangGraph (AI Agent Framework)

🧠 Ollama (MedGemma Model)

📞 Twilio (Emergency Calling)

🔥 OpenAI (LLM Orchestration)

🚀 Features

    ✅ Empathetic AI mental health conversations
    ✅ ReAct-based AI agent with tool usage
    ✅ Emergency call support via Twilio
    ✅ Therapist location recommendation tool
    ✅ Streamlit Chat UI
    ✅ FastAPI production-ready backend

🏗️ Project Architecture
User (Streamlit UI)
        ↓
FastAPI Backend (/ask endpoint)
        ↓
LangGraph ReAct Agent
        ↓
Tools:
   • MedGemma (Therapeutic Response)
   • Emergency Call (Twilio)
   • Therapist Locator

📂 Project Structure
├── frontend.py        # Streamlit UI
├── main.py            # FastAPI backend
├── ai_agent.py        # LangGraph ReAct Agent
├── tools.py           # MedGemma + Twilio tools
├── config.py          # API Keys and credentials
└── README.md

⚙️ Installation Guide
1️⃣ Clone the Repository
git clone https://github.com/yourusername/ai-mental-health-therapist.git
cd ai-mental-health-therapist

2️⃣ Create Virtual Environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

3️⃣ Install Dependencies
pip install fastapi uvicorn streamlit langchain langgraph langchain-openai ollama twilio requests

4️⃣ Setup Environment Variables

Edit config.py:

TWILIO_ACCOUNT_SID = "your_sid"
TWILIO_AUTH_TOKEN = "your_token"
TWILIO_FROM_NUMBER = "your_twilio_number"
EMERGENCY_CONTACT = "emergency_number"
OPENAI_API_KEY = "your_openai_key"


⚠️ IMPORTANT: Never push real API keys to GitHub. Use .env file in production.

5️⃣ Install & Run Ollama + MedGemma

Install Ollama from:

👉 https://ollama.com

Pull MedGemma model:

ollama pull alibayram/medgemma:4b


Run Ollama server:

ollama serve

▶️ Running the Application
Start FastAPI Backend
uvicorn main:app --reload


Backend runs at:

http://localhost:8000

Start Streamlit Frontend
streamlit run frontend.py


Frontend runs at:

http://localhost:8501
