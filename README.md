# How to Build an Advanced RAG System using LangChain

## Overview
- Learn to build an AI-powered retrieval-based question-answering (QA) system.
- Uses LangChain, Groq API, LlamaParse, and Qdrant for document processing and retrieval.
- Queries Meta’s Q1 2024 Earnings Report to extract relevant financial information.

## Prerequisites
- Install required libraries using pip.
- Libraries include LangChain, Qdrant, LlamaParse, FastEmbed, Flashrank, Unstructured[md].

## Steps in the Tutorial

### Set Up Environment Variables
- Configure Groq API Key for interacting with the language model.

### Import Required Modules
- Load necessary LangChain, Qdrant, LlamaParse, FastEmbed, Flashrank modules.

### Download and Parse the Financial Report
- Retrieve Meta’s Q1 2024 earnings report via gdown.
- Use LlamaParse to extract key financial data and save as Markdown.

### Split and Embed Documents
- Load the extracted document using UnstructuredMarkdownLoader.
- Split into smaller chunks (2048 chars) using RecursiveCharacterTextSplitter.
- Generate embeddings with FastEmbed (BAAI/bge-base-en-v1.5).
- Store embeddings in Qdrant for efficient search.

### Perform Similarity Search
- Query the document using Qdrant’s similarity search.
- Retrieve relevant sections with retriever (k=5).

### Apply Contextual Compression
- Use Flashrank to rerank retrieved documents based on relevance.
- Improve accuracy by filtering out irrelevant results.

### Build Retrieval-Based Q&A System
- Use LangChain’s RetrievalQA to generate answers.
- Integrate ChatGroq to respond with AI-generated insights.

## Outcome
- A fully functional AI agent capable of answering financial queries from Meta’s report.
- Optimized retrieval using embedding, ranking, and contextual compression.
- Hands-on experience with LangChain, vector databases, and AI retrieval models.

