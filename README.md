## 🎬 Anime Analytics Dashboards (Tableau)
---
### 📘 Overview

This Tableau project presents three interactive dashboards — By Type, By Show, and By Score — designed to explore and visualize patterns in the anime industry using the MyAnimeList Dataset from Kaggle.

The project analyzes how factors like anime type, genres, source material, and audience engagement impact popularity, ratings, and rankings.
All three dashboards are combined in one Tableau workbook:
📁 Anime_Dashboards.twb

---
### 🧾 Dataset Description

### Data Source
[MyAnimeList Dataset – DBD Mobile (Kaggle)](https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset)

Dataset Overview:
This dataset provides detailed metadata of anime titles scraped from MyAnimeList.net, including information such as ratings, genres, studios, number of episodes, and user engagement.

Stats:

~20,000 anime titles

~25 columns

Covers genres, studios, ratings, airing status, and viewer metrics

Field	Description
name	English title of the anime
genre	Comma-separated list of genres (Action, Comedy, Drama, etc.)
type	Format (TV, Movie, OVA, ONA, Special)
source	Based on original work (Manga, Light Novel, Game, Original, etc.)
episodes	Total number of episodes
duration	Average runtime (minutes per episode)
rating	Average user rating (0–10)
scored_by	Number of users who rated the anime
members	Number of users who added the anime to their list
studios / producers	Production companies involved
status	Airing status (Finished, Airing, Not yet aired)

Data Preparation Steps:

Replaced missing or null values with "Unknown".

Converted duration strings (e.g., “24 min”) into numeric format.

Split multi-valued fields like genres and studios into separate entries.

Created calculated fields for:

Popularity Index = members × scored_by

Average Episode Duration

Normalized Rank Metric

Filtered incomplete or low-data titles for better visualization quality.

---

### 📊 Dashboards & Analysis Patterns

## 1️⃣ Anime By Type Dashboard
---

### 📸 Screenshot:

![Dashboard 1](screenshots/Screenshot%20(112).png)

---

Purpose: Explore overall trends across anime types — TV, Movie, OVA, ONA, and Special.

Key Visuals:

KPI Cards: Total Anime, Avg Rating, Avg Duration, Avg Viewers

Bar Charts:

Anime count by Type

Anime count by Source (Manga, Game, Novel, etc.)

Pie / Donut Charts:

Distribution by Status (Finished, Airing)

Share of anime by Content Rating (PG-13, R, etc.)

Trend View: Average rating by year or release pattern

Insights:

TV anime dominate total production volume.

Movies and OVAs tend to have higher average ratings but smaller audiences.

Most anime originate from manga or original works.

Majority (~90%) are finished airing, indicating stable archival data

---
## 2️⃣ Anime By Show Dashboard

---
### 📸 Screenshot:

![Dashboard 2](screenshots/Screenshot%20(113).png)

---
Purpose: Provide detailed insights for individual anime titles.

Key Visuals:

Dynamic Filter: Choose any anime by name.

Information Panel: Title, type, rating, maturity, number of episodes, and synopsis.

KPI Cards: Rank, Scored By, Members, Duration, and Popularity Index.

Bar or Text Panels: Producers and genres.

Cover Image Display: Shows anime artwork for a more immersive layout.

Insights:

Fullmetal Alchemist: Brotherhood and Attack on Titan lead both ratings and viewership.

Anime in genres like Drama, Action, and Adventure consistently dominate the top ranks.

Mature-rated (R-17+) shows attract stronger engagement among dedicated viewers.

---

## 3️⃣ Anime By Score Dashboard

---

### 📸 Screenshot:

![Dashboard 3](screenshots/Screenshot%20(114).png)

---
Purpose: Compare top anime by their scores, ranks, and audience engagement.

Key Visuals:

Dual Bar Charts:

Left axis → Ratings

Right axis → Viewer counts (members)

Top N Selector: View Top 10 / Top 20 / Top 50 anime interactively.

Highlight Table: Score vs Rank comparison with consistent color encoding.

Dynamic Sorting: Sort by rating or audience count.

Insights:

Fullmetal Alchemist: Brotherhood, Hunter x Hunter (2011), and Steins;Gate are top-performing titles by both score and popularity.

Ratings above 8.5 correlate strongly with 1M+ audience engagement.

Movies and OVA formats often achieve higher per-minute ratings compared to long TV series.

---
### 🧠 Key Findings

Genre Dominance: Action, Drama, and Fantasy lead both in volume and ratings.

Source Influence: Manga-based anime dominate the top-rated and most-watched categories.

Audience Trends: Positive relationship between rating and audience size.

Runtime Consistency: Average anime episode runs between 23–25 minutes.

---
### ⚙️ Tools & Technologies
Tool	Purpose
Tableau Desktop / Public	Dashboard creation & visualization
Excel / Python (pandas)	Data cleaning & preprocessing
Kaggle (MyAnimeList Dataset)	Source dataset
Calculated Fields in Tableau	Popularity Index, Rank Normalization, Average Duration
Design Theme	Dark minimal layout with vibrant metric highlights

---
### 🚀 How to Use

Download the Tableau workbook:

Anime_Dashboards.twb


Open it using Tableau Public (Free) or Tableau Desktop.

Navigate through the dashboards:

By Type → macro trends

By Show → detailed anime analysis

By Score → rating vs popularity comparison

---
### 📂 Repository Structure

📁 Anime-Analytics-Dashboards/
├── README.md
├── Anime_Dashboards.twb
└── screenshots/
├── Anime_By_Type.png
├── Anime_By_Show.png
└── Anime_By_Score.png
     
---
### 🌱 Future Enhancements

Add time-series dashboards for anime release trends by year.

Integrate review sentiment from MyAnimeList or Reddit APIs.

Build genre correlation heatmaps (e.g., Action + Adventure frequency).

Publish a live Tableau Public version for interactive exploration.

---
