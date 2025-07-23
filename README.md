# 🎧 Music Recommendation System

This is a content-based music recommender system that suggests 5 songs similar to the one you select. It uses lyrics data and a precomputed similarity matrix. The app is deployed using Streamlit and connects to the Spotify API to fetch album art.

---

## 🧠 How It Works

1. **Lyrics-based similarity**: The system processes song lyrics using NLP techniques (tokenization + stemming).
2. **Vectorization & Similarity**: TF-IDF or count vectorization is applied, followed by a cosine similarity matrix.
3. **Recommendation Logic**: Given a song, the system finds the most similar lyrics using the similarity matrix.
4. **Spotify API**: Album cover images are fetched live using the Spotify Web API.

---

## 🗂️ Project Structure

```text
music-recommendation-system/
│
├── app.py                         # Streamlit app
├── main.ipynb                     # Preprocessing & model creation
├── df.pkl                         # Pickled song dataset
├── similarity.pkl                 # Pickled similarity matrix
├── requirements.txt               # Python dependencies
└── data/
    └── spotify_millsongdata.csv   # Original lyrics dataset
```
## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/gadjicte/Recommendation-System.git
cd Recommendation-System
```
### 2. Install Dependencies

```
pip install -r requirements.txt
```
### 3. Run the App

```
streamlit run app.py
```
## 🧠 How it Works

Load Movie Data: The dataset includes movie titles, genres, keywords, and other features.

Vectorization: Uses CountVectorizer and TF-IDF Vectorizer to convert text into numerical format.

Similarity Calculation: Computes pairwise cosine similarity between movies.

Recommendation Engine: When a user selects a movie, the system returns the top 5 most similar movies.

## 🧪 Example Output

```text
Input: Head And Heart

Top 5 Recommended Movies:
1. Anything
2. Our Love
3. Love Me
4. Is It Love
5. If You Love Me
```
## 🔧 Requirements

```bash
streamlit
pandas
scikit-learn
numpy
```
or install with:
```
pip install streamlit pandas scikit-learn numpy
```
## 📊 Dataset Citation
MovieLens 100K Dataset. GroupLens Research.
Available at: https://grouplens.org/datasets/movielens/100k/

## 🙌 Acknowledgments
GroupLens Research for the MovieLens dataset

Streamlit for interactive web app interface

scikit-learn for machine learning utilities

## 🎓 Learning Objectives
Understand content-based filtering

Use cosine similarity to compare items

Build interactive apps using Streamlit

Deploy ML apps in real-world scenarios

## 💾 Notes
Large Files: similarity.pkl and data/spotify_millsongdata.csv are tracked with Git LFS.

If you clone the repo and they’re missing, run:
```
git lfs install
git lfs pull
```
