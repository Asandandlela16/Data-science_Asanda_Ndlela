# 🎓 Student Performance Interactive Dashboard

## 📌 Project Overview

This project explores the impact of various external factors on student academic performance using a dataset from Kaggle. The dataset includes key academic metrics like math, reading, and writing marks, alongside external factors such as gender, lunch type, parental education, and race/ethnicity.

The goal was to analyze performance trends and build an **interactive dashboard** using:

- **Excel** (for data cleaning and basic processing)
- **Power BI** (for dashboard development)
- **PowerPoint** (for executive summary)

---

## 🧼 Data Preparation

- No duplicates were found.
- Created two new columns:
  - `Average Mark` = (Math + Reading + Writing) / 3
  - `Outcome`: 
    - **FAIL** if Average < 50  
    - **PASS WITH DISTINCTION** if Average ≥ 75  
    - **PASS** otherwise

## 🔍 Key Observations

1. Students with a **standard lunch break** performed better in Math.
2. **Males outperformed females** in Math by 5.1%, though females dominate among top achievers.
3. **Pass Rate**: 89.7%  
   - 324 distinctions (59% female, 41% male)
4. **Group E**: Best-performing race group with an average of 72.75%
   - **Group C** showed strong teamwork and low failure rate (only 25 out of 319 failed)

---

## ✅ Recommendations

1. **Lunch Strategy**: Lock classrooms during lunch and promote standardized lunch breaks.
2. **Gender Equity Programs**:
   - Support females facing social issues (GBV, etc.)
   - Implement study groups with gender balance and peer support.
3. **"We All Pass" Project**:
   - Offer extra support classes to all students, not just those failing.
   - Use **positive incentives**: rewards, UKZN trips, performance-based cash prizes.
4. **Lecturer Workshops**:
   - Keep track of group performance by race.
   - Promote fair assessment and diverse group activities.

---

## 🚀 Future Work

- Add machine learning models (e.g., classification or regression) to predict performance.
- Extend dataset with attendance, participation, or socio-economic variables.
- Compare with performance data across different schools or provinces.


