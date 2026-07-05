# Netflix-Dashboard
Studied and analyzed netflix dataset from kaggle. Prepared a Power BI dashboard for an interactive summary.
# 🎬 Netflix Dashboard – Power BI

## 📌 Project Overview

This project is an interactive **Power BI dashboard** built using the Netflix Movies and TV Shows dataset from Kaggle. The dashboard provides valuable insights into Netflix's content library, helping users analyze trends in content distribution, ratings, genres, countries, release years, and more.

The goal of this project is to demonstrate data cleaning, data modeling, DAX calculations, and dashboard design skills using Power BI.

---

## 📂 Dataset

**Source:** Kaggle – Netflix Movies and TV Shows Dataset

The dataset contains information such as:

* Show ID
* Title
* Type (Movie/TV Show)
* Director
* Cast
* Country
* Date Added
* Release Year
* Rating
* Duration
* Genre (Listed In)
* Description

---

## 🎯 Objectives

* Analyze Netflix's content library.
* Compare Movies vs TV Shows.
* Identify content trends over the years.
* Analyze content by country.
* Understand genre distribution.
* Explore ratings and maturity classifications.
* Create an interactive dashboard for business insights.

---

## 🛠 Tools & Technologies

* Power BI Desktop
* Power Query
* DAX (Data Analysis Expressions)
* Microsoft Excel (optional preprocessing)

---

## 📊 Dashboard Features

### KPI Cards

* Total Titles
* Total Movies
* Total TV Shows
* Total Countries
* Total Genres
* Average Release Year

### Visualizations

* Movies vs TV Shows
* Titles Added by Year
* Content Released by Year
* Top 10 Countries by Content
* Top Genres
* Ratings Distribution
* Duration Analysis
* Content Added by Month
* Top Directors
* Interactive Filters (Slicers)

---

## 📈 DAX Measures Used

```DAX
Total Titles = COUNTROWS(Netflix)

Movies =
CALCULATE(
COUNTROWS(Netflix),
Netflix[type]="Movie"
)

TV Shows =
CALCULATE(
COUNTROWS(Netflix),
Netflix[type]="TV Show"
)

Average Release Year =
AVERAGE(Netflix[release_year])

Countries =
DISTINCTCOUNT(Netflix[country])

Genres =
DISTINCTCOUNT(Netflix[listed_in])

Latest Content Year =
MAX(Netflix[release_year])
```

Additional measures can include:

* Percentage of Movies
* Percentage of TV Shows
* Running Total
* Year-over-Year Growth
* Average Duration
* Ranking using RANKX()

---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

* Removed duplicate records
* Handled missing values
* Split multiple countries into separate rows (if required)
* Standardized date formats
* Converted data types
* Removed unnecessary columns
* Cleaned genre and country names

---

## 📌 Dashboard Insights

Some key insights obtained include:

* Movies significantly outnumber TV Shows.
* The United States contributes the largest amount of Netflix content.
* Most content has been added after 2015.
* Drama and International Movies dominate the platform.
* TV-MA is one of the most common maturity ratings.
* Netflix experienced rapid content growth between 2017 and 2020.

---

## 🎨 Dashboard Interactivity

Users can filter the dashboard using:

* Country
* Content Type
* Rating
* Genre
* Release Year
* Date Added

All visuals update dynamically based on slicer selections.

---

## 📁 Project Structure

```
Netflix Dashboard/
│
├── Dataset/
│   └── netflix_titles.csv
│
├── Dashboard/
│   └── Netflix Dashboard.pbix
│
├── Images/
│   ├── Dashboard Overview.png
│   ├── Content Analysis.png
│   └── Country Analysis.png
│
└── README.md
```

---

## 🚀 Skills Demonstrated

* Data Cleaning
* Data Modeling
* Power Query
* DAX
* Data Visualization
* Dashboard Design
* Business Intelligence
* Data Storytelling
* KPI Development

---

## 📷 Dashboard Preview

> Add screenshots of your dashboard inside the **Images** folder and display them here using Markdown.

Example:

```markdown
![Dashboard Overview](Images/Dashboard%20Overview.png)
```

---

## 📚 Future Enhancements

* Sentiment analysis using descriptions
* Recommendation dashboard
* Predictive analytics
* Genre clustering
* Netflix Originals analysis
* Interactive tooltip pages
* Drill-through reports
* AI-powered insights

---

## 👩‍💻 Author

**Shubhi Pathak**

Aspiring Data Analyst | Power BI | SQL | Python | Excel

Feel free to connect or provide feedback on this project.
