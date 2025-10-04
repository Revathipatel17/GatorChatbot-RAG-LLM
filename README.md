🧠 Gator RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot with real-time web search and multi-format document ingestion, designed for intelligent question answering.
Built using LangChain, Hugging Face Transformers, FAISS/Chroma, and Gradio, it enables seamless retrieval, contextual reasoning, and explainable responses for uploaded documents and web data.

⚙️ Key Features

📚 Document Ingestion: Process PDFs, Word, Excel, and Text files for context retrieval.

🌐 Real-Time Web Search: Integrates with SerpAPI or DuckDuckGo for live data.

🧩 RAG Pipeline: Embeds documents, retrieves top-k chunks, and generates context-aware answers.

💬 Interactive Web UI: Built with Gradio featuring chat history, export, and reference display.

🧠 LLM Integration: Works with Hugging Face models like TinyLlama, falcon-7b-instruct, or distilgpt2.

🧰 Modular Architecture: Clean separation between ingestion, pipeline, and interface.

🛡️ Optional Enhancements: Guardrails, monitoring, Dockerization, and latency tracking support.

🚀 Quick Setup
1️⃣ Clone the Repository
git clone https://github.com/<your-username>/Gator-RAG-Chatbot.git
cd Gator-RAG-Chatbot

2️⃣ Create and Activate Virtual Environment
python3 -m venv venv
source venv/bin/activate       

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Add API Keys

Create a .env file in the root directory:

SERPAPI_API_KEY=your-serpapi-key

💡 How to Run
# Step 1 – Index uploaded documents
python ingestion.py

# Step 2 – Start RAG and LLM pipeline
python chatbot.py

# Step 3 – Launch Gradio Web App
python gradio_app.py


Then open your browser at → http://127.0.0.1:7861

📂 Gator-RAG-Chatbot/
🧠 ingestion.py        # Handles document loading, chunking, embeddings, vector DB
🤖 chatbot.py          # Core RAG logic and LLM integration
💬 gradio_app.py       # Web interface for chat and web search
📦 requirements.txt    # Python dependencies list
📝 README.md           # Project documentation


🧱 Technologies Used
Category	Tools / Frameworks
LLM & Embeddings	Hugging Face Transformers, SentenceTransformers
Retrieval	FAISS / Chroma Vector Store
Pipeline	LangChain
Web Search	SerpAPI / DuckDuckGo
Interface	Gradio
Environment	Python 3.10+, .env for API keys
🧪 Example Use Case

Upload research PDFs or Word files.

Ask contextual questions like:

“Summarize the main findings of the uploaded paper.”
“What are the performance metrics discussed in Section 3?”

Get an answer with citations and reference snippets.

🛠 Troubleshooting

If Excel or PDF ingestion fails:

pip install openpyxl msoffcrypto-tool pypdf

To switch LLM models:

model_name = "TinyLlama/TinyLlama-1.1B-Chat-v1.0"

👨‍💻 Author

Revathi Patel Marri
📧 revathipatel.marri0304@gmail.com

✨ A project demonstrating applied RAG and LLM engineering for knowledge retrieval, reasoning, and explainable AI.
