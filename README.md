# RAG-SHL
RAG system for SHL product catlog

#RAG system pipeline
1. Load Web Page
Uses LangChain's WebBaseLoader to scrape and load content from the SHL product catalog.

2. Split Documents
Splits large text chunks using RecursiveCharacterTextSplitter for efficient processing.

3. Embeddings
Embeds the text using sentence-transformers/all-MiniLM-L6-v2.

4. Vector Store
Embeddings are stored in ChromaDB, a fast and lightweight vector DB.

5. Local LLM
Loads google/flan-t5-base using Hugging Face Transformers to run locally (no API key).

6. RAG Chain
Creates a RetrievalQA chain that retrieves relevant documents and uses the LLM to generate responses.
