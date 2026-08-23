# Netflix Data Analysis & Power BI Dashboard

An end-to-end **Netflix Data Analysis project** using **Python, Pandas, NumPy, Matplotlib, Seaborn, and Power BI** to explore Netflix's content catalog, uncover trends, and transform raw data into meaningful business insights.

The project covers the complete data analytics workflow — from **data exploration and cleaning to feature engineering, exploratory data analysis, visualization, and interactive dashboard development**.

---

## Project Overview

Netflix hosts thousands of movies and TV shows across different countries, genres, ratings, release years, and content types.

The goal of this project is to analyze the Netflix catalog and answer questions such as:

* How many Movies and TV Shows are available?
* Which countries contribute the most content?
* What are the most common genres?
* How has Netflix content evolved over the years?
* Which ratings are most common?
* What is the distribution of movie durations?
* Which directors and actors appear most frequently?
* How much content has Netflix added over time?
* How does the content distribution vary across decades?
* What relationships exist between important numerical variables?

---

## Tech Stack

| Technology           | Purpose                         |
| -------------------- | ------------------------------- |
| **Python**           | Data analysis and preprocessing |
| **Pandas**           | Data manipulation and cleaning  |
| **NumPy**            | Numerical operations            |
| **Matplotlib**       | Data visualization              |
| **Seaborn**          | Statistical visualization       |
| **Power BI**         | Interactive dashboard           |
| **Jupyter Notebook** | Analysis environment            |
| **CSV**              | Dataset storage                 |

---

## Project Structure

```text
Netflix Data Analysis/
│
├── Dataset/
│   └── netflix_titles.csv
│
├── Cleaned_data/
│   └── clean_netflix_titles.csv
│
├── Notebook/
│   └── Netflix_Data_Analysis.ipynb
│
├── Netflix Dashboard.pbix
│
└── README.md
```

---

## Dataset

The analysis uses the **Netflix Titles Dataset**, containing information about movies and TV shows available on Netflix.

### Important Features

Some of the major columns include:

* `show_id` — Unique identifier
* `type` — Movie or TV Show
* `title` — Title of the content
* `director` — Director of the content
* `cast` — Cast members
* `country` — Country of production
* `date_added` — Date added to Netflix
* `release_year` — Original release year
* `rating` — Content rating
* `duration` — Movie duration or number of TV show seasons
* `listed_in` — Genres/categories
* `description` — Content description

---

# Project Workflow

```text
Raw Dataset
     │
     ▼
Data Exploration
     │
     ▼
Data Cleaning
     │
     ▼
Feature Engineering
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Data Visualization
     │
     ▼
Clean Dataset Export
     │
     ▼
Power BI Dashboard
     │
     ▼
Business Insights
```

---

# 1. Data Exploration

The initial stage focuses on understanding the structure and quality of the dataset.

The following checks were performed:

* Dataset shape
* Data types
* Descriptive statistics
* Sample records
* Duplicate records
* Missing values
* Column-level information

Example:

```python
df.shape
df.info()
df.describe(include="all")
df.sample(5)
df.duplicated().sum()
df.isnull().sum()
```

---

# 2. Data Cleaning

Several preprocessing techniques were applied to improve data quality.

### Duplicate Removal

Duplicate records were removed from the dataset.

```python
df.drop_duplicates(inplace=True)
```

### Missing Value Handling

Missing values in important categorical columns were handled using appropriate placeholder values.

```python
df["director"] = df["director"].fillna("Unknown")
df["cast"] = df["cast"].fillna("Unknown")
df["country"] = df["country"].fillna("Unknown")
df["rating"] = df["rating"].fillna("Not Rated")
df["duration"] = df["duration"].fillna("Unknown")
```

Records without a `date_added` value were removed where required for time-based analysis.

---

# 3. Feature Engineering

Additional features were created to make the analysis more meaningful.

### Date Features

The `date_added` column was converted into a datetime format.

New features include:

* `Year Added`
* `Month Added`
* `Day Added`

### Release Decade

Content was categorized into release decades.

Example:

```text
1980s
1990s
2000s
2010s
2020s
```

### Duration Analysis

The original duration information was separated into:

* Duration Value
* Duration Unit

Movies were additionally categorized into:

* Short Movie
* Medium Movie
* Long Movie

### Content Age

A content-age feature was created to analyze how old the content is relative to the analysis period.

### Country Count

The number of countries associated with each title was calculated.

### Genre Count

The number of genres/categories associated with each title was calculated.

---

# 4. Exploratory Data Analysis

The project explores multiple dimensions of Netflix's catalog.

## Movies vs TV Shows

Analyzed the distribution between:

* Movies
* TV Shows

This helps understand the overall composition of Netflix's content library.

---

## Top Countries

Identified the countries producing the largest number of Netflix titles.

```python
df["country"].value_counts().head(10)
```

---

## Top Genres

Analyzed the most frequently occurring genres/categories in the dataset.

This provides insight into the types of content that dominate Netflix's catalog.

---

## Content Ratings

Analyzed the distribution of Netflix content across different ratings.

Examples include:

* TV-MA
* TV-14
* PG-13
* R
* PG
* G

---

## Release Year Analysis

Analyzed the number of titles released across different years.

This helps identify periods of significant growth in Netflix's content catalog.

---

## Netflix Content Added Over Time

The project analyzes how many titles were added to Netflix each year.

This provides insight into Netflix's content expansion over time.

---

## Movie Duration Analysis

Movie durations were analyzed using a histogram to understand the distribution of movie lengths.

---

## Release Decade Analysis

Titles were grouped into decades to understand how Netflix's catalog is distributed across different eras.

---

## Top Directors

The analysis identifies directors with the highest number of titles in the dataset.

---

## Top Actors

Cast information was processed to identify actors appearing most frequently across Netflix titles.

---

## Correlation Analysis

A correlation heatmap was created using numerical variables such as:

* Release Year
* Duration
* Content Age
* Country Count

This helps identify relationships between numerical features.

---

## Movies vs TV Shows Over Time

The project compares the release trends of Movies and TV Shows across different years.

This helps visualize how the balance between the two content types has changed over time.

---

# 5. Power BI Dashboard

The cleaned dataset was also used to create an interactive **Power BI dashboard**.

The dashboard provides a visual interface for exploring Netflix's content catalog and discovering important trends.

### Dashboard Analysis Includes

* Total Netflix titles
* Movies vs TV Shows
* Content distribution
* Release trends
* Genre analysis
* Country analysis
* Rating distribution
* Content trends over time
* Interactive filtering

The Power BI dashboard is included in:

```text
Netflix Dashboard.pbix
```

---

# Key Insights

The project provides insights into:

* The overall composition of Netflix's catalog
* The balance between Movies and TV Shows
* Major content-producing countries
* Popular genres and categories
* Content rating distribution
* Netflix's content growth over time
* Distribution of content across release decades
* Movie duration patterns
* Frequently appearing directors and actors
* Trends in Movies vs TV Shows over different years

---

# Skills Demonstrated

This project demonstrates practical experience in:

### Data Analytics

* Data exploration
* Data cleaning
* Missing-value treatment
* Duplicate removal
* Data transformation
* Feature engineering
* Exploratory Data Analysis

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

### Data Visualization

* Bar charts
* Count plots
* Line charts
* Histograms
* Heatmaps
* Trend analysis

### Business Intelligence

* Power BI
* Dashboard development
* Interactive filtering
* KPI visualization
* Data storytelling

---

# How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/netflix-data-analysis.git
```

## 2. Navigate to the Project

```bash
cd netflix-data-analysis
```

## 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Or create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Then install dependencies:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Notebook/Netflix_Data_Analysis.ipynb
```

---

# Power BI

To explore the interactive dashboard:

1. Install **Power BI Desktop**
2. Open:

```text
Netflix Dashboard.pbix
```

3. Interact with the available visuals and filters.

---

# Project Highlights

```text
✓ Complete Data Analytics Workflow
✓ Python-Based Data Cleaning
✓ Exploratory Data Analysis
✓ Feature Engineering
✓ Statistical Visualization
✓ Netflix Content Trend Analysis
✓ Country & Genre Analysis
✓ Movie Duration Analysis
✓ Director & Actor Analysis
✓ Power BI Dashboard
✓ Cleaned Dataset Export
```

---

# Future Improvements

Potential extensions for this project include:

* Add advanced Power BI DAX measures
* Build more interactive dashboard pages
* Perform sentiment analysis on content descriptions
* Analyze genre combinations
* Build a Netflix content recommendation system
* Apply clustering to identify content groups
* Analyze geographic content trends
* Predict future content additions
* Build a Streamlit web application
* Deploy the analysis as an interactive web dashboard

---

# Conclusion

This project demonstrates how raw entertainment data can be transformed into meaningful insights using **Python and Power BI**.

By combining data cleaning, feature engineering, exploratory analysis, visualization, and business intelligence, the project provides a complete end-to-end example of a practical **Data Analytics workflow**.

---

## Author

**Vishal**

B.Tech — Artificial Intelligence & Robotics Engineering

### Areas of Interest

* Data Analytics
* Data Science
* Machine Learning
* Artificial Intelligence
* Python
* Business Intelligence

---

## If You Found This Project Useful

If you found this project interesting, consider giving the repository a **star** and checking out my other data analytics and machine learning projects.

**Thanks for visiting!**
