# Phishing-url-prediction
Develop an advanced machine learning model to classify URLs as either phishing or legitimate by analyzing features extracted from the URL structure, content, and metadata. This system aims to provide real-time detection of phishing attempts, enhancing cybersecurity by protecting users from malicious websites and online threats.

# 📊 **Intermediate Phase Submission**

This document summarizes the steps completed in the **Intermediate Phase** of the **Phishing-url-prediction** project. The objective of this phase was to perform an initial **Exploratory Data Analysis (EDA)** to understand the structure and distribution of the dataset.


1. **Loaded the Dataset**  
   - Successfully loaded the `PhiUSIIL_Phishing_URL_Dataset.csv` file using **pandas**.
   - Displayed the **first five rows** to verify the dataset was loaded correctly.

2. **Displayed the Dataset Shape**  
   - Printed the **shape** of the dataset to identify the number of **rows** (samples) and **columns** (features).

3. **Generated Statistical Summaries**  
   - Used the `describe()` method to present **summary statistics** (mean, median, min, max, and quartiles) for **numerical features**.
   - Checked for **missing values** and confirmed their presence, if any.

4. **Checked Skewness**  
   - Calculated the **skewness** of each numerical column to understand the **asymmetry** of data distributions.
   - Plotted **histograms** to visualize how the data is distributed.

5. **Detected Outliers Using Box Plots**  
   - Used **box plots** to identify potential **outliers** in the numeric columns.
   - Dynamically adjusted the **layout** of box plots to accommodate datasets with many features.

---

## 📌 **Libraries Used:**
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical calculations.
- **matplotlib** and **seaborn**: For data visualization (histograms and box plots).
