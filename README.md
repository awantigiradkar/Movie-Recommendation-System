# Movie Recommendation System

**Live Demo**: [Click here to try it out](https://movierecommendationsystem-tmdb.streamlit.app/)

A simple yet powerful content-based movie recommender system built using Python, Streamlit, and TMDb API. Pick a movie you like, and instantly get five personalized recommendations with posters to help you find your next watch.

---

## Features

- **Search from hundreds of movies** using a convenient dropdown.
- **Content-based filtering** using movie metadata.
- **Cosine similarity** for calculating closeness between movies.
- **Poster previews** fetched dynamically from TMDb API.
- **Fast and interactive** Streamlit interface.

---

## Tech Stack

- **Python 3**
- **Pandas**, **NumPy**, **scikit-learn**
- **Streamlit** (for UI)
- **Pickle** (for model storage)
- **TMDb API** (for fetching movie posters)

---

## How It Works

1. **Data Collection**  
   Uses TMDb 5000 Movies and Credits datasets to extract:
   - Title
   - Overview
   - Genres
   - Cast & Crew (Director)
   - Keywords

2. **Data Processing**  
   - Combined relevant textual features into a single "tags" column.
   - Converted text data into vectors using `CountVectorizer`.
   - Calculated **cosine similarity** to find movies with similar content.

3. **Fetching Data**
   - Fetches top 5 similar movies based on cosine similarity score.

4. **TMDb Poster Fetch**
   -Uses TMDb API to fetch high-quality movie posters based on movie_id.
