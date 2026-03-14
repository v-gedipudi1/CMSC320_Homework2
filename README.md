# Moral Bias in Data Science: An Analysis of CMSC320 Survey Data
**Author:** Venni Gedipudi  
**University:** University of Maryland  
**Course:** CMSC320 - Introduction to Data Science

## 📌 Project Overview
This repository contains an end-to-end data science pipeline analyzing moral judgment patterns and gender-based double standards within a longitudinal dataset (2023–2026). The project explores the "Ground Truth" problem in ethics by quantifying how the **student body** evaluates the **jerkiness** of a **protagonist** based on **gender-flipping** scenarios.

### Key Technical Features:
* **Data Preprocessing:** Automated keyword-based extraction to handle messy, unstandardized CSV headers.
* **Data Imputation:** Implementation of **Hot Deck Imputation** to handle missing values without losing data variance.
* **Feature Engineering:** Ordinal-to-Numeric transformation of qualitative survey responses.
* **Statistical Validation:** Conducted **Independent Samples T-Tests** to reject the Null Hypothesis ($H_0$).
* **Theoretical Application:** Analysis of results through the lens of **Moral Foundations Theory (MFT)**.

---

## 📊 Key Visualization
Below is the primary distribution analysis of the "Doctor Scenario." The results show a significant right-skew for female protagonists, indicating a stricter moral standard compared to their male counterparts.

![Student Moral Judgments Plot](final_analysis_plot.png)



---

## 🛠️ Installation & Usage
To replicate this analysis, ensure you have Python 3.x installed along with the following libraries:

```bash
pip install pandas numpy seaborn matplotlib scipy
