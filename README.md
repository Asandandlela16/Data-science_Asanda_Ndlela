# 🔥 California Wildfire Visualizations

## 📌 Table of Contents
1. [Project Overview](#project-overview)
2. [Project Goals](#project-goals)
3. [Data Sources](#data-sources)
4. [Tools & Technologies](#tools--technologies)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Visualizations](#visualizations)
7. [Key Insights](#key-insights)
8. [Challenges](#challenges)
9. [How to Run](#how-to-run)
10. [Folder Structure](#folder-structure)
11. [Future Work](#future-work)
12. [Author](#author)

---

## 🧠 Project Overview
This project explores historical wildfire data in California to understand the patterns, causes, and impacts of wildfires over time. Through data visualization, we aim to uncover trends and relationships in wildfire activity and present these insights in a visually compelling way.

---

## 🎯 Project Goals
- Analyze trends in wildfire frequency and severity over time.
- Identify geographic hotspots for wildfires.
- Explore seasonal and annual patterns.
- Visualize the relationship between fire size, cause, and location.

---

## 🗂️ Data Sources
- [Kaggle: Wildfire Data in California](https://www.kaggle.com/)
- [US Forest Service – Fire Occurrence Data](https://www.fs.usda.gov/)
- Additional geospatial data for mapping (if applicable)

**Note:** Some datasets were cleaned, merged, and transformed to create a consistent structure for analysis.

---

## 🛠 Tools & Technologies
- **Python:** pandas, matplotlib, seaborn, plotly, geopandas
- **Jupyter Notebook**
- **Power BI / Tableau** (optional, for dashboards)
- **Git & GitHub**
- **VS Code**

---

## 📊 Exploratory Data Analysis (EDA)
- Trends in number of wildfires per year
- Distribution of wildfire sizes
- Most common causes of fires (human vs. natural)
- Monthly and seasonal patterns
- Regional analysis by county or coordinates

---

## 📈 Visualizations
- 📉 Line Chart: Wildfires per Year
- 🔥 Bar Chart: Top 10 Fire Causes
- 🌍 Heatmap: Fires by Region
- 🗺️ Choropleth Map: Total Area Burned by County
- 📅 Seasonal Trends: Wildfires by Month

Visuals are available in the `visuals/` folder and in the Jupyter Notebooks.

---

## 🔍 Key Insights
- Wildfires peak between **July and September**, correlating with dry summer conditions.
- **Human-caused** wildfires are the leading contributor to large-scale fire damage.
- Certain counties in **Northern California** experience consistently higher fire incidents.
- Over the years, the **average wildfire size** has increased.

---

## 🧩 Challenges
- Missing or inconsistent geospatial data in some records.
- Datasets with different formats and units required preprocessing.
- Large datasets required performance optimization during plotting.

---

## ⚙️ How to Run
1. Clone the repository:
