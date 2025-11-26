# 🎧 Spotify Tracks EDA — Exploratory Data Analysis  

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)  
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)  
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

> A detailed exploratory data analysis on Spotify track data to uncover musical trends, popularity patterns, and the characteristics that make songs successful.

---

## 📘 Project Overview  

This project focuses on **Exploratory Data Analysis (EDA)** of Spotify track data. It aims to identify relationships between **audio features** (like energy, valence, danceability) and a song’s **popularity**, uncovering trends across decades and genres.  

The study reveals how **modern music** differs from older eras — becoming **shorter, more energetic, less acoustic**, and more **dance-focused** — while offering insights useful for music producers, analysts, and data scientists.

---

## 🎯 Objectives  

The primary goals of this analysis were:
- To understand the **distribution** of key musical features (popularity, energy, danceability, valence, etc.)
- To explore **relationships** between popularity and musical characteristics.
- To examine **temporal trends** (year-wise analysis).
- To identify **top-performing tracks and artists**.
- To derive **recommendations** for model design or music success strategies.

---

## 📊 Dataset Summary  

| Feature | Description |
|----------|--------------|
| `track_id` | Unique Spotify track identifier |
| `track_name` | Song title |
| `artist_name` | Artist name |
| `year` | Year of release |
| `popularity` | Popularity score (0–100) |
| `danceability` | Suitability for dancing |
| `energy` | Intensity of the song |
| `valence` | Positiveness or musical mood |
| `acousticness` | Degree of acoustic elements |
| `instrumentalness` | Likelihood of instrumental-only |
| `speechiness` | Spoken word presence |
| `tempo` | Beats per minute (BPM) |
| `duration_ms` | Song length in milliseconds |
| `language` | Detected lyric language |
| `loudness`, `mode`, `key`, `time_signature` | Musical composition features |

---

## 🔍 Univariate Analysis  

- **Popularity** → Highly skewed; most songs have low scores, few are global hits.  
- **Danceability** → Left-skewed; majority are rhythmic and danceable.  
- **Energy** → Concentrated near 1.0; most tracks are high-energy.  
- **Valence** → Bimodal; both happy and neutral/sad songs exist widely.  
- **Tempo** → Bimodal peaks around 120 and 140 BPM.  
- **Duration** → Mostly 3–5 mins; extreme outliers exist.  
- **Loudness** → Unreliable feature due to data errors.  
- **Instrumentalness** → Dominated by vocal tracks (≈0).  

---

## 🔗 Bivariate Analysis  

- **Popularity vs Danceability** → Popular songs have Danceability > 0.4.  
- **Popularity vs Energy** → Low Energy = low popularity; high Energy ≠ guaranteed success.  
- **Popularity vs Duration** → Negative correlation; short songs perform better.  
- **Popularity vs Valence** → Mood doesn’t predict hits.  
- **Energy vs Loudness** → Highly correlated; redundant.  
- **Danceability vs Tempo** → Weak relationship; tempo not a predictor.  
- **Energy vs Popularity Category** → High/Medium hits have higher energy.  
- **Danceability vs Popularity Category** → Hits more danceable and consistent.  
- **Valence vs Popularity Category** → Mood uniform across categories.  

---

## 🧠 Correlation Insights  

| Feature | Correlation with Popularity |
|----------|------------------------------|
| Energy | 0.15 |
| Valence | 0.15 |
| Danceability | 0.14 |
| Acousticness | -0.14 |
| Instrumentalness | -0.13 |

✅ **Recommendation:** Drop redundant pairs — Energy-Loudness (0.90), Valence-Danceability (0.64).  

---

## 📅 Temporal Trends  

- **Energy ↑** — Music became more intense since 1970s.  
- **Valence ↓** — Songs became less positive post-1995.  
- **Danceability ↑** — Spike after Disco era (1980s).  
- **Speechiness ↑ (2020s)** — Rise in rap/spoken content.  
- **Acousticness ↓** — Shift to electronic music post-1990s.  
- **Duration ↓** — Songs shorter in streaming age.  
- **Popularity Distribution** — >80% of tracks are low popularity.  

---

## 🌍 Language & Artist Analysis  

- **Korean** tracks have highest average popularity (~27.5).  
- **Hindi** ranks next (~18.5); **Malayalam** lowest (~7).  
- **Artists by Volume:** Shankar Mahadevan, Ramin Djawadi, Alan Silvestri (film composers).  
- **Artists by Popularity:** Rihanna, Taylor Swift, Kendrick Lamar, LE SSERAFIM (mainstream hits).  

---

## 💡 Key Takeaways  

1. ✅ **Use Classification Models:** Predict “Hit” or “Miss” instead of regression on scores.  
2. 🧹 **Data Cleaning:** Remove soundtrack composers and outliers.  
3. ⚡ **Apply Feature Filters:** Exclude songs with very low energy/danceability.  
4. 🎭 **Combine Mood Features:** Use interaction of energy × valence.  
5. 🔁 **Feature Reduction:** Drop redundant variables (e.g., Loudness).  

---

## ⚙️ Tech Stack  

- **Language:** Python 3.11  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Plotly  
- **Environment:** Jupyter Notebook  

---

## 🚀 Run Instructions  

```bash
git clone https://github.com/yourusername/spotify-eda.git
cd spotify-eda
pip install -r requirements.txt
jupyter notebook
```


---

## 📈 Future Work  

- Build classification model for hit prediction.  
- Add time-series trend forecasting.  
- Sentiment analysis using lyrics.  
- Create interactive dashboard (Streamlit/Dash).  

---

## 👤 Author  

**Joy Talukdar**  
 
