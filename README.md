
# Document-Based Question Answering System

This project is a Document-based Question Answering System built using Google Gemini API and LangChain, deployed using Streamlit and served publicly via Ngrok. It enables users to upload a document, process it using chunking and embeddings, and ask contextually relevant questions. The system provides intelligent answers using a large language model.

## Features

- Upload and parse documents
- Chunk and embed document text using Google Gemini Embeddings
- Retrieve context-aware answers via LangChain's retrieval chain
- Integrated with Google Gemini 2.5 Pro model for content generation
- Deployable on Streamlit and sharable via Ngrok tunneling

## Stack Used

- Frontend: Streamlit
- Backend: Python, LangChain
- LLM: Google Gemini 2.5 Pro (via LangChain)
- Embeddings: GoogleGenerativeAIEmbeddings
- Vector DB: FAISS
- Utilities: Ngrok, dotenv, PyPDF

## Setup Instructions

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Set up your `.env` or `secrets.toml` for API keys (Streamlit Cloud users must use `secrets.toml`):

```toml
# .streamlit/secrets.toml
GEMINI_API_KEY = "your_google_gemini_api_key"
```

3. Run the app:

```bash
streamlit run app.py
```

4. If using Ngrok:

```bash
ngrok config add-authtoken YOUR_AUTH_TOKEN
ngrok http 8501
```

## Deployment

You can deploy the app for free using:
- Streamlit Cloud: https://streamlit.io/cloud
- Ngrok (for local development sharing)
