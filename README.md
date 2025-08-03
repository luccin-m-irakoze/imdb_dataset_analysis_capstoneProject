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

Notebook: data_prep.ipynb

---

## Power BI Dashboard

### Features:
- Line chart: Rating trends over years
- Bar chart: Top 10 genres by count
- Pie chart: Rating class distribution
- Scatter plot: Runtime vs Rating
- Slicers: Year, Genre, Rating Category
- KPI Cards: Average rating, total high-rated movies

Power BI file: imdb_dashboard.pbix

---

## 💡 Innovation

- Used `class_weight='balanced'` to address class imbalance
- Included `numVotes` as a popularity feature
- Exported ML results to visualize in Power BI
- Focused on interpretability and real-world relevance

---

## How to Run

1. Open `data_prep.ipynb` in Jupyter Notebook or VS Code
2. Run all cells to clean, analyze, and model the data
3. Load `imdb_predictions.csv` into Power BI
4. Open `imdb_dashboard.pbix` to view interactive visuals

---

## Screenshots 

Add screenshots of your:

- Python output (plots):
<img width="1083" height="537" alt="image" src="https://github.com/user-attachments/assets/251a3c7e-f5f2-4f7d-b548-9585a531d294" />
<img width="774" height="572" alt="image" src="https://github.com/user-attachments/assets/8afda0a8-06c6-4dee-a932-43b573fff774" />
<img width="982" height="724" alt="image" src="https://github.com/user-attachments/assets/c1ddf697-aefd-461b-af5f-cc0ca1194e3f" />
<img width="981" height="730" alt="image" src="https://github.com/user-attachments/assets/746036e8-8962-4216-991a-ff348d80f3cb" />
<img width="1088" height="642" alt="image" src="https://github.com/user-attachments/assets/091e31be-4976-4b1b-9b6e-cc04a003c9ab" />

- Power BI dashboard
<img width="1353" height="771" alt="image" src="https://github.com/user-attachments/assets/491f1a0e-57c1-4a49-b8b9-6bd9f61071f0" />
<img width="668" height="776" alt="image" src="https://github.com/user-attachments/assets/e221b071-828f-4fae-908d-443fe9f645c3" />
<img width="1373" height="770" alt="image" src="https://github.com/user-attachments/assets/ac3e2511-1075-45bb-9fdf-f281c48e7cd8" />
<img width="1291" height="770" alt="image" src="https://github.com/user-attachments/assets/f0f59a14-c132-420b-9f04-ec75e29c00a5" />
<img width="1374" height="964" alt="image" src="https://github.com/user-attachments/assets/13c7ad1a-f938-45d7-b8c7-69d8938b9796" />

---

## Project Structure

    /data/
        imdb_predictions.csv
    /notebooks/
        data_prep.ipynb  
    /powerbi/
        imdb_dashboard.pbix      
    /presentation/
        capstone_slides.pptx    
    README.md


---

##  Acknowledgments

Thanks to [IMDb Datasets](https://www.imdb.com/interfaces/) for providing open data for academic use.

---


