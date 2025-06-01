# 🎬 Movie Recommendation System

This project builds a **Content-Based Movie Recommendation System** using metadata from the TMDB 5000 Movies and Credits dataset. The system recommends movies similar to a user-specified title based on features like genres, keywords, cast, and crew.

## 📂 Dataset

The system uses two datasets:
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

These are merged on the `title` column and relevant fields are extracted for further analysis.

## ⚙️ Features Used

- **Genres**
- **Keywords**
- **Cast (Top 3)**
- **Director (from Crew)**
- **Overview**

These features are processed and combined into a single textual metadata string to compute similarity between movies.

## 🧠 Methodology

- **Data Preprocessing**: Null values removed, JSON strings parsed.
- **Feature Extraction**: Using Python's `ast` and `pandas`.
- **Vectorization**: TF-IDF or CountVectorizer.
- **Similarity Metric**: Cosine similarity to compare vectorized movie metadata.
- **Recommendation**: Top 5 similar movies to a given input movie.

## 🧪 Example

```python
recommend("Avatar")
```

**Output**:
```
['John Carter', 'Battle: Los Angeles', 'Aliens', 'Titan A.E.', 'The Matrix']
```

## 📦 Requirements

Install dependencies with:

```bash
pip install pandas numpy scikit-learn
```

Run the notebook with:

```bash
jupyter notebook movies_recommendation_system.ipynb
```

## 📁 File Structure

```
movies_recommendation_system.ipynb   # Jupyter Notebook with the recommendation system
tmdb_5000_movies.csv                 # Movie metadata
tmdb_5000_credits.csv                # Credits (cast & crew)
```
