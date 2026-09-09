# VOIS-Major-Project-Agriculture-Analysis

**VOIS AICTE Batch 1 (2026–2027) - Major Project**[cite: 4]  
**Student Name:** Sutirtha Giri[cite: 5]  
**College Name:** Netaji Subhash Engineering College[cite: 5]  
**AICTE Student ID:** STU6a6050cd2e1271784697037[cite: 5]  

---

## 📌 Project Overview
This project investigates agricultural performance across three primary cropping seasons: **Kharif**, **Rabi**, and **Zaid**[cite: 4]. By evaluating 4,000 farm records across 28 distinct attributes, the study analyzes the impact of seasonal weather variations, irrigation methods, and input costs on crop output and net farm profitability[cite: 4, 5].

---

## 🎯 Key Questions Addressed
* How do crop yield and net profit vary across different cropping seasons?[cite: 4]
* What are the environmental determinants (rainfall, humidity, temperature) of seasonal performance?[cite: 4]
* Which irrigation techniques maximize water efficiency and economic returns?[cite: 4]
* Are profitability differences across seasons statistically significant?[cite: 4]

---

## 🛠️ Tech Stack & Environment
* **Programming Language:** Python[cite: 5]
* **Data Manipulation:** Pandas, NumPy[cite: 5]
* **Data Visualization:** Matplotlib, Seaborn[cite: 5]
* **Statistical Analysis:** SciPy (`scipy.stats`)[cite: 5]
* **Development Platform:** Google Colab[cite: 5]

---

## ⚙️ Data Preprocessing & Analysis Pipeline

1. **Data Cleaning & Imputation:**
   * Handled missing entries in `Rainfall_mm` (48), `Soil_Moisture_pct` (40), and `Yield_Tonnes_Ha` (32)[cite: 4, 5].
   * Filled missing environmental variables using seasonal medians to prevent seasonal distortion[cite: 4, 5].
   * Recalculated missing crop yields using the formula: $\text{Production\_Tonnes} / \text{Farm\_Area\_Hectares}$[cite: 4, 5].

2. **Feature Engineering:**
   * **Profit Margin (%):** $(\text{Profit\_INR} / \text{Revenue\_INR}) \times 100$[cite: 4]
   * **Cost per Hectare:** $\text{Total\_Cost\_INR} / \text{Farm\_Area\_Hectares}$[cite: 4]

3. **Exploratory Data Analysis (EDA):**
   * **Univariate Analysis:** Evaluated feature spread and skewness for `Profit_INR` and `Rainfall_mm` using KDE distribution plots[cite: 4, 5].
   * **Bivariate Analysis:** Compared crop yield and profit across seasons, assessed water consumption by irrigation method, and analyzed crop profitability[cite: 4, 5].

4. **Statistical Hypothesis Testing:**
   * Performed a One-Way ANOVA test across Kharif, Rabi, and Zaid profit figures to validate statistical significance ($p < 0.05$)[cite: 4, 5].

---

## 📊 Key Findings

* **Seasonal Profit Disparity:**
  * **Kharif:** Highest average profit of **₹1,78,914.65**, supported by favorable monsoon conditions[cite: 4].
  * **Rabi:** Consistent yield output with an average profit of **₹87,689.47**[cite: 4].
  * **Zaid:** Negative net returns (**-₹24,804.82**) due to extreme summer heat and high resource/irrigation costs[cite: 4].

* **Statistical Significance:**
  * One-Way ANOVA yielded an **F-Statistic of 34.29** and a **P-Value of $1.71 \times 10^{-15}$**, confirming that seasonal profit differences are statistically significant[cite: 4, 5].

* **Irrigation Efficiency:**
  * **Drip Irrigation:** Delivers the highest average profit (**₹2,19,626.00**) with strong water efficiency (6.27 t/1,000 m³)[cite: 4, 5].
  * **Flood Irrigation:** Consumes the highest water volume (~8,026 m³) while yielding lower profits (**₹73,354.02**)[cite: 4, 5].

* **Crop Economics:**
  * Cash crops (Sugarcane and Chilli) delivered the highest net margins across all seasons[cite: 4, 5].
  * Staple grains (Wheat and Rice) operated on narrower margins under standard cultivation costs[cite: 4, 5].

---

## 💡 Practical Recommendations
1. **Promote Drip Irrigation:** Transitioning from flood to drip irrigation saves approximately 25% water while substantially increasing net profit[cite: 5].
2. **Mitigate Summer Deficits:** Discourage high-water crops during Zaid; prioritize heat-tolerant, drought-resilient crops[cite: 5].
3. **Preventive Kharif Pest Control:** Deploy pre-monsoon pest surveillance to prevent yield loss during high-humidity periods (54.47% risk peak)[cite: 4, 5].

---

## 📁 Repository Structure
```text
├── seasonal_agriculture_performance_dataset.csv                   # Project dataset
├── VOIS_Major_Project_Seasonal_Agriculture_Performance_Analysis.ipynb  # Jupyter Notebook
├── VOIS_Major_Project_PPT_Submission_Template_Completed.pptx     # Presentation slides
├── Problem_Statement.pdf                                          # Project problem statement
└── README.md                                                      # Project documentation
