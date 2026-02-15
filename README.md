🧠AI Mental Health Therapist

    An AI-powered Mental Health Support System that provides empathetic conversations, therapist recommendations, and emergency assistance.

Built using:

    ⚡ FastAPI – Backend API

    🎨 Streamlit – Interactive Chat UI

    🤖 LangChain + LangGraph – ReAct AI Agent

    🧠 Ollama (MedGemma Model) – Local therapeutic LLM

     📞 Twilio – Emergency Calling Support

     🔥 OpenAI – LLM Orchestration

 ✨Features

     💬 Warm, empathetic AI mental health conversations

     🛠 ReAct-based intelligent tool selection

     📍 Therapist recommendation by location

     🚨 Automatic emergency call trigger for crisis situations

     🎨 Clean Streamlit chat interface

     ⚡ FastAPI production-ready backend

🏗️ Architecture

            User (Streamlit UI)
                    ↓
            FastAPI Backend (/ask)
                    ↓
            LangGraph ReAct Agent
                    ↓
            Tools Layer:
               • MedGemma (Therapeutic AI)
               • Therapist Locator
               • Emergency Call (Twilio)




📂 Project Structure


    ├── frontend.py        # Streamlit UI
    ├── main.py            # FastAPI backend
    ├── ai_agent.py        # ReAct Agent logic
    ├── tools.py           # MedGemma + Twilio integration
    ├── config.py          # API keys (DO NOT COMMIT REAL KEYS)
    └── README.md

🚀 Installation & Setup

    1️⃣ Clone the Repository
            git clone https://github.com/yourusername/ai-mental-health-therapist.git
            cd ai-mental-health-therapist
            

    2️⃣ Create Virtual Environment
            python -m venv venv
            source venv/bin/activate   # Windows: venv\Scripts\activate

    3️⃣ Install Dependencies
            pip install fastapi uvicorn streamlit langchain langgraph langchain-openai ollama twilio requests

    4️⃣ Configure API Keys

    Update config.py:

    TWILIO_ACCOUNT_SID = "your_sid"
    TWILIO_AUTH_TOKEN = "your_token"
    TWILIO_FROM_NUMBER = "your_twilio_number"
    EMERGENCY_CONTACT = "emergency_number"
    OPENAI_API_KEY = "your_openai_key"



5️⃣ Setup Ollama + MedGemma

Install Ollama from:

    https://ollama.com

Pull the MedGemma model:

    ollama pull alibayram/medgemma:4b


Run Ollama:

    ollama serve

▶️ Running the Application
Start Backend
uvicorn main:app --reload


Backend runs at:

    http://localhost:8000

Start Frontend
streamlit run frontend.py


Frontend runs at:

    http://localhost:8501

🧠 How It Works

    The system uses a ReAct AI Agent that decides which tool to use:

     Tool	Purpose
    ask_mental_health_specialist	Generates therapeutic responses using MedGemma
    find_nearby_therapists_by_location	Suggests local therapists
    emergency_call_tool	Triggers emergency call via Twilio

    The AI prioritizes safety and emotional support.

💡 Example Prompts

    “I feel anxious and overwhelmed.”

    “Can you find a therapist in Delhi?”

    “I want to harm myself.”

    The agent responds appropriately and triggers emergency support if needed.

🔒 Disclaimer

    This project is for educational and demonstration purposes only.

    It is NOT a replacement for licensed mental health professionals.
    If someone is in immediate danger, contact local emergency services immediately.

🛠 Tech Stack

    Python 3.10+

    FastAPI

    Streamlit

    LangChain

    LangGraph

    Ollama

