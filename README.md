# Book Recommendation System with LLM

This project builds a book recommendation system using a local Large Language Model (LLM) and FAISS (Facebook AI Similarity Search) for vector storage. The system is designed to recommend books based on metadata from the "7k Books" dataset available on Kaggle. We use Ollama serve for the local LLM and embedding model, ensuring quick and efficient recommendations. The project combines the power of FAISS for fast similarity searches with the ability of an LLM to understand and embed complex text data.

## Dataset

The dataset used for this project is the [7k Books with Metadata](https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata) from Kaggle, which provides metadata for over 7,000 books, including titles, authors, and genres. This metadata serves as the foundation for our recommendation engine.

## How It Works

1. **Data Preparation**: We load the 7k Books dataset and process the metadata to create book embeddings using the local LLM through Ollama serve.
2. **FAISS Vector Database**: FAISS is used to store and search through the book embeddings, enabling efficient nearest-neighbor lookups to find similar books based on the embeddings.
3. **Recommendation System**: Given a book as input, the system retrieves the most similar books by querying the FAISS vector index.

## Requirements

To run this project, you will need the following Python libraries:

```bash
pip install pandas==2.2.2 numpy==1.26.3 faiss-cpu==1.8.0 requests==2.32.3 rich tqdm

```

