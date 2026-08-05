# YouTube Video Summarization using Retrieval-Augmented Generation (RAG)

An intelligent AI-powered application that generates accurate and context-aware summaries of YouTube videos using **Retrieval-Augmented Generation (RAG)**. The system extracts video transcripts, converts them into vector embeddings, retrieves the most relevant context using **FAISS**, and generates concise summaries through a Large Language Model (LLM).

---

## Overview

Understanding long-form YouTube content can be time-consuming. This project automates the summarization process by combining transcript retrieval, semantic search, and LLM-based text generation to produce high-quality summaries while preserving contextual accuracy.

The application leverages a Retrieval-Augmented Generation (RAG) pipeline, allowing the language model to generate responses based on retrieved transcript segments instead of relying solely on its pre-trained knowledge.

---

## Features

- Extracts transcripts from YouTube videos
- Performs semantic text chunking for efficient retrieval
- Generates vector embeddings using Hugging Face models
- Stores embeddings in a FAISS vector database
- Retrieves relevant transcript chunks through similarity search
- Produces context-aware summaries using an open-source Large Language Model
- Modular architecture suitable for extending to question answering or chatbot applications

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Framework | LangChain |
| Transcript Extraction | YouTube Transcript API |
| Embedding Model | Hugging Face Sentence Transformers |
| Vector Database | FAISS |
| Language Model | Llama.cpp (GGUF Model) |
| Environment | Google Colab |
| Utilities | Python Dotenv, Tiktoken |

---

## System Architecture

```text
                YouTube Video
                      │
                      ▼
        Transcript Extraction
                      │
                      ▼
        Recursive Text Chunking
                      │
                      ▼
        Embedding Generation
                      │
                      ▼
          FAISS Vector Store
                      │
                      ▼
        Similarity-Based Retrieval
                      │
                      ▼
       Large Language Model (LLM)
                      │
                      ▼
          AI Generated Summary
```

---

## Project Workflow

1. Retrieve the transcript of a YouTube video.
2. Split the transcript into semantically meaningful chunks.
3. Generate embeddings for each chunk using a Hugging Face embedding model.
4. Store the embeddings in a FAISS vector database.
5. Retrieve the most relevant transcript sections using similarity search.
6. Provide the retrieved context to the language model.
7. Generate a concise and contextually accurate summary.

---


---

## Required Packages

```text
youtube-transcript-api
langchain
langchain-community
langchain-text-splitters
langchain-huggingface
sentence-transformers
faiss-cpu
llama-cpp-python
huggingface_hub
python-dotenv
tiktoken
```

---

## Usage

1. Configure the Hugging Face API token.
2. Provide the YouTube video URL or Video ID.
3. Fetch the transcript.
4. Generate vector embeddings.
5. Build the FAISS vector index.
6. Generate an AI-powered summary from the retrieved context.

---

---

## Key Concepts

- Retrieval-Augmented Generation (RAG)
- Semantic Search
- Vector Embeddings
- FAISS Similarity Search
- Context-Aware Text Generation
- Natural Language Processing (NLP)

---

## Future Enhancements

- Interactive Streamlit Web Application
- Support for multilingual transcripts
- Timestamp-aware summaries
- Question Answering over YouTube videos
- Chapter-wise summarization
- Support for multiple embedding models
- Integration with cloud vector databases (Pinecone, Qdrant)

---

## Sample Output

**Input**

```
https://www.youtube.com/watch?v=<video_id>
```

**Generated Output**

- Executive summary of the video
- Key discussion points
- Important insights
- Actionable takeaways

---

