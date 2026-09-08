#📚 PDF Semantic Search with Pinecone

A hands-on Vector Database project that demonstrates how to process a PDF, convert its text into embeddings, store those embeddings in Pinecone, and perform semantic similarity search.

## 🚀 Project Overview

This project uses an Artificial Intelligence PDF as the knowledge source.

The PDF is processed into smaller text chunks, converted into vector embeddings using a Sentence Transformer model, and stored in a Pinecone vector index.

A user query is then converted into an embedding and compared against the stored vectors to retrieve the most semantically relevant sections of the PDF.

## 🔄 Workflow

PDF
↓
Text Extraction
↓
Text Chunking
↓
Embedding Generation
↓
Pinecone Vector Database
↓
Query Embedding
↓
Semantic Similarity Search
↓
Top-K Relevant Chunks

## 🧠 Technologies Used

- Python
- Google Colab
- PyPDF
- Sentence Transformers
- Pinecone
- Vector Embeddings
- Semantic Search

## 📌 What I Learned

- How to extract text from PDF documents
- Why large documents are divided into chunks
- How text is converted into numerical embeddings
- How vector embeddings represent semantic meaning
- How to create and configure a Pinecone index
- How to store vectors using upsert
- How to perform similarity search
- How to retrieve the most relevant document chunks using Top-K search
- How metadata can be stored alongside vectors

## 🔎 Example

A query such as:

"What is Breadth First Search?"

is converted into an embedding and sent to Pinecone.

Pinecone searches the stored vectors and returns the most semantically similar chunks from the PDF.

## 🏗️ Project Architecture

```text
                    AI PDF
                      │
                      ▼
                Text Extraction
                      │
                      ▼
                  Chunking
                      │
                      ▼
             Sentence Transformer
                      │
                      ▼
              384-D Embeddings
                      │
                      ▼
                  Pinecone
                      │
                ┌─────┴─────┐
                │           │
             Storage      Search
                            ▲
                            │
                         Query
                            │
                    Query Embedding
                            │
                            ▼
                    Top-K Results
