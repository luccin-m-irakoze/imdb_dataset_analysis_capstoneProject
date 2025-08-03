# **IMDb Movie Ratings Analysis**

**Course**: INSY 8413 – Introduction to Big Data Analytics  

**Academic Year**: 2024–2025, Semester III  

**Lecturer**: Eric Maniraguha  

**Student**: Munezero Irakoze Luccin

**Sector**: Entertainment  

---

## Project Overview

This project explores trends in IMDb movie ratings using open public datasets. The goal was to identify key factors that influence whether a movie is highly rated (IMDb score ≥ 7) and to build a predictive model using Python. Visual insights were created using Power BI.

---

## Dataset Details

- **Title**: IMDb Open Data  
- **Source**: [IMDb Datasets](https://www.imdb.com/interfaces/)  
- **Files Used**: `title.basics.tsv.gz`, `title.ratings.tsv.gz`  
- **Size**: ~58,000 filtered movie records  
- **Format**: Structured (.tsv)  
- **Status**: Required preprocessing (merging, filtering, cleaning)

---

## Python Analysis (Jupyter Notebook)

### Steps Completed:
1. **Data Cleaning**:
   - Filtered for movies only
   - Dropped rows with missing values
   - Converted columns to numeric (year, runtime)
   - Merged ratings data by `tconst`
2. **Exploratory Data Analysis**:
   - Top genres and their average ratings
   - Ratings trends over time
   - Scatter plots of rating vs runtime and votes
3. **Machine Learning Model**:
   - **Algorithm**: Logistic Regression (`class_weight='balanced'`)
   - **Features**: `runtimeMinutes`, `startYear`, `numVotes`
   - **Target**: Binary classification of `highRated` (1 if IMDb rating ≥ 7)
   - **Accuracy**: ~52%
   - **Recall (High Rated)**: 72%
4. **Exported cleaned and predicted data** for Power BI

Notebook: [`imdb_analysis.ipynb`](./imdb_analysis.ipynb)

---

## Power BI Dashboard

### Features:
- Line chart: Rating trends over years
- Bar chart: Top 10 genres by count
- Pie chart: Rating class distribution
- Scatter plot: Runtime vs Rating
- Slicers: Year, Genre, Rating Category
- KPI Cards: Average rating, total high-rated movies

Power BI file: [`imdb_dashboard.pbix`](./imdb_dashboard.pbix)

---

## 💡 Innovation

- Used `class_weight='balanced'` to address class imbalance
- Included `numVotes` as a popularity feature
- Exported ML results to visualize in Power BI
- Focused on interpretability and real-world relevance

---

## How to Run

1. Open `imdb_analysis.ipynb` in Jupyter Notebook or VS Code
2. Run all cells to clean, analyze, and model the data
3. Load `imdb_cleaned.csv` or `imdb_predictions.csv` into Power BI
4. Open `imdb_dashboard.pbix` to view interactive visuals

---

## Screenshots (optional)

Add screenshots of your:
- Python output (plots)
- Power BI dashboard

---

## Submission Summary

- Jupyter notebook
- Power BI dashboard
- Cleaned dataset
- GitHub repo with README
- PowerPoint presentation

---

##  Acknowledgments

Thanks to [IMDb Datasets](https://www.imdb.com/interfaces/) for providing open data for academic use.

---


