📚 RAG Pipeline from Scratch (Python + FAISS)

A minimal, modular Retrieval-Augmented Generation (RAG) pipeline built from scratch using Python and FAISS, focused on understanding how document retrieval and LLM-based generation work together under the hood.

This project avoids heavy abstractions and frameworks to clearly demonstrate the core mechanics of RAG systems.

🧠 What is RAG?

Retrieval-Augmented Generation (RAG) enhances large language models by:

Retrieving relevant information from custom documents

Injecting that context into the prompt

Generating grounded responses, reducing hallucinations

This allows LLMs to answer questions using your own data, not just pre-training knowledge.

🚀 What This Project Does

✔ Loads documents from local files
✔ Converts text into vector embeddings
✔ Stores embeddings in a FAISS vector store
✔ Performs semantic similarity search
✔ Generates summarized, context-aware answers

🏗️ Project Structure
rag-pipeline-from-scratch/
│
├── Project 1/
│   ├── app.py                # Main pipeline entry point
│   ├── src/
│   │   ├── data_loader.py    # Document loading & preprocessing
│   │   ├── vectorstore.py    # FAISS vector store logic
│   │   ├── search.py         # Retrieval + generation logic
│   │
│   ├── data/                 # Input documents
│
├── requirements.txt
├── pyproject.toml
├── README.md

🔁 RAG Pipeline Flow

Load documents from the data/ directory

Split text into manageable chunks

Generate embeddings for each chunk

Store embeddings in a FAISS index

Retrieve top-K relevant chunks for a query

Generate a summarized response using retrieved context

🛠️ Tech Stack

Python 3.11+

FAISS (vector similarity search)

LLM APIs (configurable)

Modular, framework-agnostic design

▶️ How to Run Locally
1️⃣ Create a virtual environment
python -m venv .venv
.venv\Scripts\activate    # Windows

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Run the pipeline
python app.py

🧪 Example Query
query = "What is an attention mechanism?"


Output:

Summary: Attention mechanisms allow models to focus on the most relevant parts of the input sequence...

📌 Design Philosophy

Built from first principles

No unnecessary abstractions

Easy to read, debug, and extend

Emphasis on understanding how RAG works internally

This makes the project ideal for learning, interviews, and portfolio demonstration.

🔮 Possible Enhancements

Add FastAPI endpoints (/ingest, /query)

Experiment with chunk sizes and overlap

Metadata-based filtering

Hybrid search (BM25 + vectors)

Simple UI using Streamlit or Gradio

👨‍💻 Author

Shivam Rustagi
Building in public | AI • RAG • Agentic Systems

⭐ Why This Project?

This project was created to deeply understand Retrieval-Augmented Generation beyond tutorials, focusing on how retrieval, embeddings, and generation interact in real systems.
