# 📺 Netflix Data Analysis

## 📌 About Netflix

Netflix is one of the most popular video streaming platforms, with over **222 million subscribers** globally (as of mid-2021). It offers a vast catalog of **10,000+ TV shows and movies** from various countries. This dataset includes detailed information such as cast, directors, ratings, release year, duration, genres, and more.

---

## 🎯 Business Problem

Analyze the Netflix dataset to generate **actionable insights** that help Netflix:
- Decide which type of shows/movies to produce.
- Identify key markets and genres.
- Grow its user base across different countries.

---

## 📁 Dataset Information

The dataset provides metadata about Netflix's content library.

### 🔗 Dataset Link  
[Raw Netflix CSV file](https://github.com/PatraRupali/EDAOnNetflix/blob/main/Netflix_raw_data.csv)

### 🧾 Columns Description

- `show_id`: Unique ID for every movie/show  
- `type`: Movie or TV Show  
- `title`: Title of the content  
- `director`: Director of the show/movie  
- `cast`: List of actors  
- `country`: Country of production  
- `date_added`: Date content was added to Netflix  
- `release_year`: Year of release  
- `rating`: TV rating  
- `duration`: Runtime or number of seasons  
- `listed_in`: Genre(s)  
- `description`: Summary  

---

## 🧹 Process Overview

### 1. 🧼 Data Cleaning

- Treated missing values with suitable defaults or imputation.  
- Unpacked comma-separated fields into individual rows for granular analysis. 
- Standardized data formats and cleaned text fields for consistency.
 

📄 [Netflix_Datacleaning.ipynb](https://github.com/PatraRupali/EDAOnNetflix/blob/main/Netflix_Datacleaning.ipynb)  
📄 [Cleaned Netflix CSV](https://github.com/PatraRupali/EDAOnNetflix/blob/main/Netflix_cleaned_dataset.csv)

---

### 2. 📊 Exploratory Data Analysis (EDA)

- Performed visual and statistical exploration of key variables.  
- Included summary statistics for numeric features and analyzed categorical distributions.
- Used heatmaps to explore correlation between year_added and release_year.
- Created custom modular functions (Analyze_column_distribution, Analyze_top_categories, plot_line_for_column, etc.) for reproducible univariate and trend analysis.
- Visualized patterns and trends using bar charts, line plots, and comparative dashboards across countries.
 

📄 [EDA on Netflix.ipynb](https://github.com/PatraRupali/EDAOnNetflix/blob/main/EDA%20on%20Netflix.ipynb)

#### 🔍 Steps

- **Data Cleaning**: Handled missing values, unstacked comma-separated columns, and standardized data  
- **Univariate Analysis**: Used the function `Analyze_column_distribution` to analyze and visualize unique values within a column  
- **Top Categories Comparison**: Utilized `Analyze_top_categories` to compare the top N categories (e.g., countries, genres) for TV shows and movies  
- **Trend Visualization**: Employed the `plot_line_for_column` function to visualize trends in data based on numeric columns (e.g., release year,year_added,month added,week_added)  
- **Correlation Analysis**: Used heatmaps to find correlations between columns, such as the relationship between the year added and the release year  
- **Country-based Analysis**: Created `Analyze_column_distribution_by_country` to analyze and compare data distribution across key countries (e.g., US, India, UK, South Korea, Japan)
---

## 📌 Key Insights

- **Top Countries**: Most content comes from **US, India, UK, Canada, France**  
- **Content Type**: ~70% Movies, ~30% TV Shows  
- **Top Directors**: Marcus Raboy, Martin Campbell, Toshiya Shinohara  
- **Top Actors**: Anupam Kher, Shah Rukh Khan (dominated by Indian actors)  
- **Popular Genres**: International Movies, Drama, Comedy  
- **Duration Trends**:  
  - Movies: Median ≈ 1h 40min  
  - TV Shows: Median = 1 season  
- **Genre Trends**: Anime and Classical Movies are gaining popularity  
- **Country-specific Genre Preference**:  
  - US: Drama, Comedy  
  - India: International Movies  
  - UK: British TV Shows  
  - Japan: Anime  
- **Director-Actor Combos**: Certain combinations are repeatedly successful  
- **TV vs Movies by Country**: TV Shows are more popular in Japan & South Korea  

---

## 💡 Recommendations for Netflix

- Focus investment on content for **top 5 countries**  
- Collaborate with **top-performing directors and actors**  
- Invest in **country-specific genre preferences**  
- Create content with **ideal duration formats** (around 100 mins or short seasons)  
- Increase **content volume**—new content additions have declined post-2019  
- Focus on **Anime and Classical genres** globally  
- Prefer **TV-Y and TV-G** ratings for new productions  
- In countries like Japan and South Korea, promote **more TV shows**

---

## ✅ Status

Project Completed ✔️  
Insights generated from data will help enhance Netflix’s strategic decisions.
