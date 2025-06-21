# Document-based Question Answering System

This project is a Document-based Question Answering (QA) System built using LangChain and Gemini Pro. It enables users to upload documents and ask context-based questions, receiving accurate answers using embedded document context.

## Features

- Upload and process documents with automatic chunking
- Convert PDF or text input into vector embeddings using Google's Gemini model
- Use FAISS for storing and retrieving document chunks efficiently
- Answer user queries by matching document context with questions
- Web UI built using Streamlit for user interaction

## Tech Stack

- Python
- LangChain
- FAISS (Facebook AI Similarity Search)
- Google Generative AI (Gemini Pro for embeddings and response generation)
- Streamlit (for building the web interface)
- Pyngrok (for creating public URL)

## How It Works

1. Upload a document via the Streamlit interface.
2. The document is read, split into chunks, and embedded using Gemini embeddings.
3. The chunks are stored in a FAISS vector database.
4. User queries are matched with relevant document chunks.
5. The system generates an answer using Gemini based on the retrieved context.

## Local Deployment

To run the project locally:

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Usage

- Upload a document (PDF or text).
- Enter a question related to the uploaded document.
- View the generated answer and context.

## Limitations

- Free-tier Gemini API quotas may restrict the number of queries per day.
- ngrok may limit concurrent tunnels for free accounts.

## License

This project is for educational purposes only.
