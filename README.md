# 🎵 Spotify Complete Master Analytics Dashboard

Welcome to the **Spotify Complete Master Analytics Dashboard** repository! This project focuses on end-to-end data processing, exploratory data analysis (EDA), advanced feature engineering, and building an interactive **3x3 KPI & Analytics Master Dashboard** using Python and Plotly.

---

## 📌 Project Overview
The goal of this project is to transform raw music dataset tracks into clean, actionable, and visual insights. By handling missing data, treating outliers, and creating custom music metrics, this project highlights key patterns in artist performance, genre trends, track popularity, language distribution, and audio characteristics.

---

## 🎯 Key Objectives
- **Data Quality & Cleaning:** Detect and impute missing values using median grouping strategies and handle statistical outliers using the Interquartile Range ($IQR$).
- **Feature Engineering:** Create new audio metrics such as duration in minutes (`duration_min`) and energy-to-danceability ratios (`energy_dance_ratio`).
- **Exploratory Data Analysis (EDA):** Identify top-performing artists, most popular genres, release year trends, and language distributions.
- **Interactive Visualizations:** Build a full standalone interactive 3x3 dashboard powered by **Plotly** (`plotly_dark` theme) and **Seaborn**.

---

## 🧰 Tools & Technologies
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Plotly (Express & Graph Objects), Seaborn, Matplotlib
- **Environment:** Jupyter Notebook / VS Code / Interactive HTML Export

---

## 📊 Dataset Metadata & Features
The dataset contains metadata and audio feature measurements for Spotify tracks:

| Feature Name | Description |
| :--- | :--- |
| `track_id` | Unique identifier for each song |
| `artist_name` | Name of the performing artist |
| `genre` | Music category/genre |
| `popularity` | Song popularity score |
| `stream_count` | Total streams on the platform |
| `danceability` | Suitability of track for dancing |
| `energy` | Perceived intensity and activity |
| `duration_ms` | Track duration in milliseconds |
| `language` | Language of the track |
| `explicit` | Content rating (Explicit vs. Clean) |

---

## 🔄 Project Workflow

### 1. Data Cleaning & Preprocessing
- **Duplicate Removal:** Verified zero duplicate records across the dataset.
- **Categorical Imputation:** Replaced missing values in `artist_name`, `genre`, `album_type`, and `language` with `'Unknown'`.
- **Numerical Imputation:** Applied median imputation grouped by `genre` to maintain distribution integrity.
- **Outlier Handling:** Calculated $IQR = Q3 - Q1$ and applied boundary clipping to trim extreme values without losing data context.

### 2. Feature Engineering
- **`duration_min`**: Converted `duration_ms` to minutes for better readability (Average duration: 3.5 min).
- **`energy_dance_ratio`**: Calculated ratio between energy and danceability scores to evaluate track dynamics.

### 3. Key Performance Indicators (KPIs)
The top section of the master dashboard highlights 9 core metrics arranged in a 3x3 layout:
1. **Total Tracks:** 10,000
2. **Total Artists:** 25
3. **Total Music Hours:** 583.3 h
4. **Average Popularity:** 50
5. **Avg Track Duration:** 3.5 min
6. **Avg Streams per Track:** 47.16 M
7. **Total Streams:** 471.59 B
8. **Total Genres:** 12
9. **Total Languages:** 12

### 4. Visualizations & Interactive Dashboard
- **Top 10 Artists:** Horizontal bar chart highlighting top-performing artists by stream count.
- **Yearly Trends:** Line chart displaying stream trends and popularity evolution over release years.
- **Genre Popularity:** Bar chart comparing average popularity scores across genres.
- **Clean vs. Explicit:** Comparison chart breaking down content ratings across tracks.
- **Album Type Share:** Donut/Pie chart showing the proportion of Albums, Singles, and Unknown types.
- **Streams by Language:** Horizontal bar chart analyzing listener engagement across languages (English, Spanish, Arabic, French, Korean, German, Portuguese, Japanese, etc.).

---

## 📈 Interactive Dashboard Preview
The project exports a fully standalone interactive dashboard notebook and HTML file: `Spotify_Master_Dashboard.html`. Users can hover over data points, filter legends, zoom in, and inspect exact metrics dynamically.

---

## 📂 Project Structure
```text
Spotify-Data-Analysis/
├── data/
│   └── spotify_data_10k.xlsx
├── notebooks/
│   └── Spotify (Plotly).ipynb
├── Spotify_Master_Dashboard.html
└── README.md
