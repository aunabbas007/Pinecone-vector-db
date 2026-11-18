# PDF Semantic Search with Pinecone

A hands-on vector database project that turns PDF content into embeddings, stores the vectors in Pinecone, and retrieves relevant text chunks for natural-language queries.

## Retrieval pipeline
```text
PDF
 ↓
Text extraction
 ↓
Chunking
 ↓
Sentence Transformer embeddings
 ↓
Pinecone vector index
 ↓
Query embedding
 ↓
Similarity search
 ↓
Top-K relevant chunks
```

## Components
- PDF text extraction with PyPDF.
- Text chunking before embedding.
- Sentence Transformers for vector generation.
- Pinecone for vector storage and similarity search.
- Metadata stored alongside vectors.

## Run
Install the dependencies used by the notebook:
```bash
pip install pinecone sentence-transformers pypdf
```

Open the notebook in Google Colab or Jupyter. Configure your Pinecone API key securely using an environment variable or notebook secret; never hard-code credentials or commit them.

## Example query
`What is Breadth First Search?`

The query is embedded and compared with stored document vectors. The nearest chunks are returned as semantic-search results.

## Stack
Python · PyPDF · Sentence Transformers · Embeddings · Pinecone · Google Colab

## Learning focus
Chunking strategy, embedding dimensions, vector indexing, metadata, similarity search, and Top-K retrieval.

## Author
[Aun Abbas](https://github.com/aunabbas007)
