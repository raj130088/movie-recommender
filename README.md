# Movie Recommender System

This is a content-based movie recommender system built using Python, Streamlit, and machine learning techniques. The app suggests movies similar to a user-selected movie and displays their posters using the OMDb API.

## Features
- Select a movie from a dropdown list.
- Get 5 recommended movies based on similarity.
- Movie posters fetched automatically using OMDb API.
- Simple, interactive UI built with Streamlit.

## Files
- `app.py`: Streamlit app that runs the movie recommender.
- `movie_dict.pkl`: Contains movie metadata (movie_id, title, tags).
- `similarity.pkl`: Precomputed similarity matrix (not included in the repo).
- `requirements.txt`: Python dependencies.
- `Movie Recommender.ipynb`: Jupyter/Colab notebook with the machine learning code to generate the similarity matrix.

## Dataset

This project uses the **TMDB Movie Metadata** dataset from Kaggle:  
[TMDB Movie Metadata Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

Steps:
1. Download the dataset from Kaggle.  
2. Use the dataset in the model-building notebook (`.ipynb` file).  
3. The notebook generates:
   - `movie_dict.pkl` → metadata about movies  
   - `similarity.pkl` → similarity matrix (not included in repo due to size)  

## How it Works
1. Movie metadata (title, genres, tags) is vectorized using **TF-IDF**.
2. A **cosine similarity matrix** is computed between all movies.
3. For a selected movie, the system finds the top 5 most similar movies.
4. Posters for recommended movies are fetched from the OMDb API.

## Note on `similarity.pkl`
The project requires a file called `similarity.pkl`, which stores the similarity matrix for all movies.  
- This file is **not included in the repository** because of size restrictions.  
- To generate it, run the provided `Movie Recommender.ipynb` notebook. It will compute the matrix and save it using `pickle`.  
- Once generated, place the file in the root directory alongside `app.py` and `movie_dict.pkl`.

## Setup Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/raj130088/movie-recommender.git
   cd movie-recommender
