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
- **Country-based Analysis**: Created `Analyze_column_distribution_by_country`and `Analyze_column_trends_by_country` to analyze and compare data distribution across key countries (e.g., US, India, UK,Canada, South Korea, Japan)
---

## 📊 Key Insights

### 📌 Content Type Distribution
- **Movies**: ~69.5%  
- **TV Shows**: ~30.5%  
➡️ *Movies dominate the catalog, but TV Shows have grown significantly since 2017.*

---

### 🌍 Country-wise Content Production
- **Top Contributors**: United States, India, United Kingdom, Japan, Canada  
- **Movie Powerhouses**: US, India  
- **TV Show Leaders**: US, UK, Japan (anime-heavy), South Korea  
➡️ *The US dominates both categories, but regional content is rising.*

---

### 🧑‍🎤 Cast & 🎬 Director Dominance
- **Top Movie Actors**: Anupam Kher, Shah Rukh Khan, Naseeruddin Shah, Samuel L. Jackson  
- **Top TV Show Voice Actors**: Takahiro Sakurai, Grey Griffin, David Attenborough  
- **Top Directors**: Rajiv Chilaka, Jan Suter, Martin Scorsese, Ken Burns  
➡️ *Distinct cast-director influence by region — Bollywood in India, anime voice actors in Japan, documentary icons in the UK/US.*

---

### 🎞️ Genre Distribution
- **Movies**: Dramas, Comedies, International, Documentaries  
- **TV Shows**: International TV, Dramas, Comedies, Docuseries, Kids’ TV  
➡️ *Strong global storytelling focus with an increasing share of binge-worthy and regional genres.*

---

### ⏱️ Duration Trends
- **Movies**: Most titles are 80–120 minutes  
- **TV Shows**: Majority are 1–3 seasons, with fewer long-running series  
➡️ *Concise formats preferred globally, though some regions enjoy longer formats (e.g., India, Japan).*

---

### 🗓️ Temporal Patterns

#### 📆 Year Added
- Major spikes between **2018–2021**, especially in **2019 (Movies)** and **2020 (TV Shows)**  
- Correlation between release year and addition year = **0.38**  
➡️ *Content is becoming fresher — added to Netflix soon after release.*

#### 📅 Month Added
- Peaks in **January, July, and December**  
➡️ *Aligned with holidays and global breaks.*

#### 📈 Week Added
- **Week 1, 13, and 44** see the most content drops  
➡️ *Bulk additions hint at strategic release cycles.*

---

### 🔞 Ratings Analysis
- **Dominant Rating**: TV-MA (Adult content)  

**Regional Rating Patterns**:
- 🇮🇳 India → TV-14, TV-MA  
- 🇯🇵 Japan → TV-14, TV-MA, PG  
- 🇺🇸 US → Full range (TV-Y to R)  

➡️ *The platform is adult-content-heavy but offers family-friendly options.*

---

### 🌐 Country vs Genre Preferences

| Country     | Movie Focus                | TV Show Focus                    |
|-------------|----------------------------|----------------------------------|
| 🇺🇸 USA      | Dramas, Comedies, Docs     | Comedies, Kids, Docuseries       |
| 🇮🇳 India    | International, Dramas      | TV Dramas, International Shows   |
| UK UK       | Documentaries, Dramas      | British TV, Documentaries        |
| 🇯🇵 Japan    | Anime, Action              | Anime, International/Korean TV   |
| SK S. Korea | Comedies, Dramas           | Romantic K-Dramas                |
| 🇨🇦 Canada   | Anime, Documentaries       | Anime Series, Kids’ TV           |

➡️ *Country-specific preferences strongly shape genre popularity and casting.*

---

## 💡 Strategic Recommendations

| Area                 | Action                                                                 |
|----------------------|------------------------------------------------------------------------|
| 🎥 Content Mix       | Prioritize movies while expanding serialized TV content                |
| 🌍 Regional Strategy | Focus on India, Japan, South Korea, and UK for regional content growth |
| 🎭 Talent Strategy   | Promote recurring cast/director powerhouses for regional engagement    |
| 📅 Timing Strategy   | Schedule releases in Jan, Jul, Dec to maximize seasonal viewership     |
| 🧒 Audience Balance  | While adult content is strong, increase Kids & Teen categories         |
| ⌛ Duration Format    | Favor short formats; selectively support long series for retention     |
| 🎞️ Genre Focus       | Double down on Dramas, International content, and Documentaries        |
| 📈 Data Strategy      | Leverage release vs added correlation to stay timely and relevant      |

---

## 📁 Project Scope

- ✅ Cleaned & preprocessed **200K+ Netflix records**  
- ✅ Analyzed & visualized trends using **Python (pandas, matplotlib, seaborn)**  
- ✅ Generated time-based, country-based, and genre-based dashboards  
- ✅ Delivered actionable insights and strategic recommendations

---

> 🎯 *This EDA enables Netflix (or any OTT platform) to better align content strategies with user preferences across countries, formats, and time.*
> 
## ✅ Status

Project Completed ✔️  
Insights generated from data will help enhance Netflix’s strategic decisions.
