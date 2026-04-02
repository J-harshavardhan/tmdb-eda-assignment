# 🎬 TMDB Movie Data Pipeline & EDA

> A data pipeline project built as part of my Data Analytics assignment (B.Tech).

---

## 📌 About the Project

In this project, I built a small end-to-end data pipeline using the **TMDB (The Movie Database) API**.  
The pipeline fetches live trending movie data, stores it in a **SQLite database**, and then performs **Exploratory Data Analysis (EDA)** using pandas.

---

## 🔄 Pipeline Flow
```
Fetch from TMDB API → Store in SQLite → Load Back → Analyze with Pandas
```

---

## 📊 What I Did

| Step | Task |
|------|------|
| Step 1 | Imported libraries & loaded API key securely via Colab Secrets |
| Step 2 | Fetched **40 movies** from TMDB Discover Movies endpoint (2 pages × 20) |
| Step 3 | Converted JSON response into a **pandas DataFrame** |
| Step 4 | Saved the data into a **SQLite database** (`movies` table) |
| Step 5 | Loaded the data back from SQLite |
| EDA 1 | Displayed first 5 rows + summary statistics |
| EDA 2 | Counted number of movies per genre |
| EDA 3 | Checked for missing values |

---

## 🔍 Key Findings

- 🥇 **Thriller** is the most common genre — appeared in **15 out of 40** movies
- 🎭 **Comedy** and **Horror** follow with **11 movies** each
- ✅ The dataset had **0 missing values** — clean data straight from TMDB
- 📈 Vote counts vary a lot — from just a few votes to **21,000+**

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Main programming language |
| Requests | Calling the TMDB API |
| Pandas | Data analysis and EDA |
| SQLite3 | Local database storage |
| Google Colab | Development environment |

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/J-harshavardhan/tmdb-eda-assignment.git
```

2. Open `tmdb_eda.ipynb` in Google Colab or Jupyter Notebook

3. Get a free API key from 👉 https://www.themoviedb.org/settings/api

4. Replace the API key at the top of the notebook:
```python
API_KEY = "your_tmdb_api_key_here"
```

5. Run all cells from top to bottom (**Runtime → Run All**)

---

## 📁 Repository Structure
```
tmdb-eda-assignment/
│
├── tmdb_eda.ipynb    # Main Jupyter Notebook (pipeline + EDA)
└── README.md         # Project documentation
```

---

## ⚠️ Note on API Key

The API key is **not hardcoded** in the notebook.  
It is stored securely using **Google Colab Secrets** and accessed via:
```python
from google.colab import userdata
API_KEY = userdata.get("TMDB_API_KEY")
```

---

## 👤 Author

**J. Harshavardhan**  
B.Tech Student | Aspiring Data Analyst  
GitHub: [@J-harshavardhan](https://github.com/J-harshavardhan)
