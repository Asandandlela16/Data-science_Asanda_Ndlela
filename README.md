


# 🫀 Heart Attack Risk Analysis & Visualization

A data-driven project aimed at analyzing patterns and biomarkers associated with heart attacks using multiple tools — Python, Excel, and Power BI. The goal was to identify significant indicators and create visualizations that aid medical understanding and decision-making.

---

## 📌 Tools & Technologies

- **Python** – Data exploration & preprocessing (`pandas`)
- **Excel** – Pivot tables, slicers, statistical comparison
- **Power BI** – Data transformation, DAX measures, interactive dashboards

---

## 🔍 Python: Data Exploration & Cleaning

- Imported the dataset using `pandas`
- Explored summary statistics with `.describe()`, including:
  - Mean heart rate
  - Identification of the oldest individual (103 years old)
- Checked for missing values using `.isnull().sum()` and filled them using `.fillna()` for clean analysis

---

📊 Excel: Statistical Pattern Analysis

- Built 5 Pivot Tables focusing on key biomarkers:
  - Troponin: A highly specific protein marker for heart muscle injury
  - CK-MB: An enzyme released during cardiac damage
- Utilized **Excel slicers** to filter by test results (positive/negative)

🔬 Key Insight:
| Test Result | Gender | CK-MB Average  |
|-------------|--------|----------------|
| Positive    | Female | 23.75          |
| Positive    | Male   | 23.05          |
| Negative    | Male   | 2.65           |
| Negative    | Female | 2.40           |

- Indicates that individuals who tested **positive** produce this enzyme at a significantly higher rate

📎 _Excel workbook available in the project files_

---

## 📈 Power BI: Dynamic Visualization & DAX

- Used **Power Query Editor** to transform data:
  - Converted data types (e.g., text → whole numbers)
  - Removed already explored columns (Troponin, CK-MB) to reduce redundancy
- Created a custom **DAX Measure**:

```DAX
Total Blood Pressure = SUM('Table'[Systolic_BP]) + SUM('Table'[Diastolic_BP])


           
