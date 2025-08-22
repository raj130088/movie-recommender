# Movie Recommender System

A simple **content-based movie recommendation system** built with **Python, Streamlit, and scikit-learn**.  
It suggests similar movies based on movie metadata (like tags, genres, and descriptions).

---

## Features
- Select a movie and get **5 recommended movies** instantly.
- Uses **cosine similarity** on TF-IDF vectors of movie tags.
- Fetches posters dynamically via the **OMDb API**.
- Simple **Streamlit UI** for interaction.

---

## Tech Stack
- **Python**
- **Pandas / NumPy**
- **scikit-learn**
- **Streamlit**
- **OMDb API**

---
## Note on `similarity.pkl`

This project requires a file called `similarity.pkl`, which contains the precomputed similarity matrix for movies.  

- The file is not included in this repository because it is too large.  
- To generate it yourself, you can run the Jupyter/Colab notebook `Movie Recommender.ipynb`, which explains the full training process.  
- Alternatively, you can compute it by applying **TF-IDF vectorization** on the movie tags dataset and then calculating the cosine similarity matrix.  

Once generated, place the `similarity.pkl` file in the project root directory alongside `app.py` and `movie_dict.pkl`.
---

## How to Run Locally
1. Clone the repo:
   ```bash
   git clone https://github.com/raj130088/movie-recommender.git
   cd movie-recommender
