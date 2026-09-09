# Seasonal Agriculture Performance Analysis

**VOIS AICTE Batch 1 (2026–2027) - Major Project**
* **Student Name:** Sutirtha Giri
* **College Name:** Netaji Subhash Engineering College

---

##  Project Overview
This project investigates agricultural performance across three primary cropping seasons: **Kharif**, **Rabi**, and **Zaid**. By evaluating 4,000 farm records across 28 distinct attributes, the study analyzes the impact of seasonal weather variations, irrigation methods, and input costs on crop output and net farm profitability

---

##  Key Questions Addressed
* How do crop yield and net profit vary across different cropping seasons?
* What are the environmental determinants (rainfall, humidity, temperature) of seasonal performance?
* Which irrigation techniques maximize water efficiency and economic returns?
* Are profitability differences across seasons statistically significant?

---

##  Tech Stack & Environment
* **Programming Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Statistical Analysis:** SciPy (`scipy.stats`)
* **Development Platform:** Google Colab

---

##  Data Preprocessing & Analysis Pipeline

### 1. Data Cleaning & Imputation
* Handled missing entries in `Rainfall_mm` (48), `Soil_Moisture_pct` (40), and `Yield_Tonnes_Ha` (32).
* Imputed missing environmental variables using seasonal medians to prevent cross-seasonal distortion.
* Recalculated missing crop yields using the formula: Production / Area.

### 2. Feature Engineering
* **Profit Margin (%):** `(Profit_INR / Revenue_INR) * 100`
* **Cost per Hectare:** `Total_Cost_INR / Farm_Area_Hectares`

### 3. Exploratory Data Analysis (EDA)
* **Univariate Analysis:** Evaluated feature spread and skewness for `Profit_INR` and `Rainfall_mm` using KDE distribution plots.
* **Bivariate Analysis:** Compared crop yield and profit across seasons, assessed water consumption by irrigation method, and analyzed crop profitability.

### 4. Statistical Hypothesis Testing
* Performed a One-Way ANOVA test across Kharif, Rabi, and Zaid profit figures to validate statistical significance (p < 0.05.

---

## 📊 Key Findings

* **Seasonal Profit Disparity:**
  * **Kharif:** Highest average profit of **₹1,78,914.65**, supported by favorable monsoon conditions.
  * **Rabi:** Consistent yield output with an average profit of **₹87,689.47**.
  * **Zaid:** Negative net returns (**-₹24,804.82**) due to extreme summer heat and high resource/irrigation costs.

* **Statistical Significance:**
  * One-Way ANOVA yielded an **F-Statistic of 34.29** and a **P-Value of 1.71e-15**, confirming that seasonal profit differences are statistically significant.

* **Irrigation Efficiency:**
  * **Drip Irrigation:** Delivers the highest average profit (**₹2,19,626.00**) with strong water efficiency (6.27 t/1,000 m³).
  * **Flood Irrigation:** Consumes the highest water volume (~8,026 m³) while yielding lower profits (**₹73,354.02**).

* **Crop Economics:**
  * Cash crops (Sugarcane and Chilli) delivered the highest net margins across all seasons.
  * Staple grains (Wheat and Rice) operated on narrower margins under standard cultivation costs.

---

## 💡 Practical Recommendations
1. **Promote Drip Irrigation:** Transitioning from flood to drip irrigation saves approximately 25% water while substantially increasing net profit.
2. **Mitigate Summer Deficits:** Discourage high-water crops during Zaid; prioritize heat-tolerant, drought-resilient crops.
3. **Preventive Kharif Pest Control:** Deploy pre-monsoon pest surveillance to prevent yield loss during high-humidity periods (54.47% risk peak).

---

## 📁 Repository Structure
```text
├── seasonal_agriculture_performance_dataset.csv
├── VOIS_Major_Project_Seasonal_Agriculture_Performance_Analysis.ipynb
├── VOIS_Major_Project_PPT_Submission_Template_Completed.pptx
├── Problem_Statement.pdf
└── README.md
