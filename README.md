🧠 AI Agent with LangChain Tools

A modular AI agent built using **LangChain + OpenAI GPT-4o-mini** that can autonomously use tools for web search, Wikipedia lookup, and saving research outputs.

This project demonstrates how modern LLM agents can interact with external tools to perform multi-step reasoning and research tasks.

**Features**

-  Web search using DuckDuckGo
-  Wikipedia knowledge retrieval
-  Save structured outputs to text files
-  Tool-using LLM agent (GPT-4o-mini)
-  Modular tool architecture (`tools.py`)
-  Environment-based API key management

**Project Structure**

AI Agent Tutorial/
│
├── main.py # Main agent execution logic
├── tools.py # Custom tools (search, wiki, save)
├── requirements.txt # Python dependencies
├── .gitignore # Ignored files (env, cache, venv)
├── .env # API keys (NOT pushed to GitHub)
└── README.md

**How It Works:**

1. User inputs a question
2. The LLM (GPT-4o-mini) analyzes the request
3. The agent selects appropriate tools:
   - DuckDuckGo → real-time web search
   - Wikipedia → factual knowledge retrieval
   - Save tool → stores results locally
4. The agent combines tool outputs into a final response

**Architecture:**

User Query
   ↓
LangChain Agent (GPT-4o-mini)
   ↓
Decision Engine (Tool Selection)
   ↓
 ┌───────────────┬───────────────┬───────────────┐
 │ Web Search    │ Wikipedia     │ File Saver    │
 │ (DuckDuckGo)  │ (API)         │ (Local TXT)   │
 └───────────────┴───────────────┴───────────────┘
   ↓
Final Structured Response

**Installation**

Clone the repository:


bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO

Install dependencies:

pip install -r requirements.txt

**Environment Setup**

Create a .env file in the root directory:

OPENAI_API_KEY=your_openai_api_key_here

**Run the Project**
python main.py

**Example Use Case**

Input:

What are the latest developments in AI agents?

Agent Behavior:

Searches web for latest info
Cross-checks Wikipedia
Summarizes findings
Optionally saves results to file

Tech Stack**
Python 
LangChain 
OpenAI GPT-4o-mini
DuckDuckGo Search
Wikipedia API

Author

Samin Morshed
AI / ML Engineer in progress
