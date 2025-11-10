# Vibe Matcher — AI-Powered Fashion Recommendation Prototype

## Overview
Vibe Matcher is a lightweight AI recommendation system that transforms subjective style descriptions into measurable product similarity.  
Users can enter natural-language queries such as "energetic urban chic" and receive the top three matching fashion items based on semantic similarity.

This project was developed as part of the Nexora AI Challenge 2025 to demonstrate how embeddings and vector search can bridge emotional language and personalization.

## Features
- Mock dataset of 5–10 fashion products with tags and descriptions  
- Text embeddings using SentenceTransformers (simulating text-embedding-ada-002)  
- Cosine similarity for top-3 recommendation ranking  
- Evaluation across multiple queries with similarity metrics  
- Latency tracking and scoring threshold analysis  
- Reflection on edge cases and future improvements such as Pinecone integration

## Tech Stack
- Python 3.10+  
- Pandas, NumPy  
- scikit-learn (cosine similarity)  
- SentenceTransformers  
- Matplotlib, timeit (evaluation and latency tracking)  
- Optional: OpenAI API (text-embedding-ada-002) for real embeddings

## Notebook Workflow
1. Data Preparation – create a small dataset of 5–10 mock fashion products  
2. Embedding Generation – compute embeddings for product descriptions and queries  
3. Vector Search – calculate cosine similarity between query and products  
4. Ranking – display top three matching items with similarity scores  
5. Evaluation – run multiple queries and track similarity and latency  
6. Reflection – document insights, limitations, and improvement ideas  

## Example Query
Input: "energetic urban chic"  
Output:  
1. Streetwear Jacket (similarity 0.84)  
2. Retro Sneakers (similarity 0.79)  
3. Cropped Denim Jacket (similarity 0.75)

## Future Improvements
- Integrate OpenAI embeddings (text-embedding-ada-002)  
- Store and retrieve vectors using Pinecone or FAISS  
- Add hybrid ranking that combines semantic and tag-based similarity  
- Implement fallback recommendations for low-similarity cases  
- Optimize batch embedding for lower latency

## Why AI at Nexora
Nexora applies AI to make personalization more human.  
The Vibe Matcher prototype demonstrates how semantic embeddings can interpret emotional intent and connect it to products.  
It converts subjective style cues into objective similarity scores, creating a meaningful link between what users feel and what they discover.

## How to Run in Google Colab
1. Open the Vibe Matcher Notebook (.ipynb file).  
2. Run setup cells to install dependencies.  
3. If using OpenAI embeddings, enter your API key securely:
   ```python
   import os
   from getpass import getpass
   os.environ["OPENAI_API_KEY"] = getpass("Enter your OpenAI API key: ")
4.Execute each section in order.
5.Review similarity scores and latency results at the end.
   
