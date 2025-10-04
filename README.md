🐊 Gator RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot with real-time web search and multi-format document ingestion, built using LangChain, Hugging Face, FAISS/Chroma, and Gradio.

✅ Features

📂 Ingest PDFs, DOCX, TXT, CSV, and XLSX files for question answering

🌐 Real-time web search integration (SerpAPI / DuckDuckGo)

🧠 Hugging Face LLMs (TinyLlama, distilgpt2, or configurable models)

💬 User-friendly Gradio chat interface with tabs for RAG and Web Search

📄 Displays references & sources alongside answers

📦 Modular design (chatbot.py, ingestion.py, gradio_app.py)

🛡️ Extendable for hallucination guardrails, Docker, and logging

🚀 Setup Instructions
1. Clone the Repository
git clone <your-repo-url>
cd RAG_Chatbot

2. Create Virtual Environment
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

4. Add API Keys

Create a .env file in the project root:

SERPAPI_API_KEY=your-serpapi-key

🧪 Run the Application
python ingestion.py     # Index documents
python chatbot.py       # Run RAG pipeline
python gradio_app.py    # Launch UI


Then visit: http://127.0.0.1:7861

📂 Project Structure
RAG_Chatbot/
1. chatbot.py         
2. ingestion.py       
3. gradio_app.py       
4. requirements.txt    
5. README.md

📝 Notes

Install extra dependencies if needed:

pip install openpyxl msoffcrypto-tool pypdf


To switch models, edit chatbot.py:

model_name = "TinyLlama/TinyLlama-1.1B-Chat-v1.0"
