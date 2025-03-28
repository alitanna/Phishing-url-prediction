# Phishing-url-prediction
Develop an advanced machine learning model to classify URLs as either phishing or legitimate by analyzing features extracted from the URL structure, content, and metadata. This system aims to provide real-time detection of phishing attempts, enhancing cybersecurity by protecting users from malicious websites and online threats.

#  **Intermediate Phase Submission**

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

##  **Libraries Used:**
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical calculations.
- **matplotlib** and **seaborn**: For data visualization (histograms and box plots).

### Data Cleaning & Preprocessing (Phase 1)  

After completing the **Intermediate Phase**, the following steps were carried out to further clean and preprocess the dataset before model training:  

---

### **1️⃣ Handling Correlated Features**  
- Identified and removed highly correlated features to prevent redundancy and multicollinearity.  
- **Removed Features:** `NoOfJS`, `NoOfExternalRef`  

---

### **2️⃣ Handling Missing Values**  
- Checked for missing values in all columns.  
- **Result:** No missing values were found in the dataset.  

---

### **3️⃣ Addressing Class Imbalance (SMOTE)**  
- **Before Balancing:**  
  - Legitimate URLs (`1`): **83,380**  
  - Phishing URLs (`0`): **57,629**  
- Applied **Synthetic Minority Over-sampling Technique (SMOTE)** to balance the dataset.  
- **After Balancing:**  
  - Both classes now have **83,380** samples each.  

---

### **4️⃣ Top-Level Domain (TLD) Analysis**  
- **Visualized the distribution of TLDs** (e.g., `.com`, `.org`) using a **horizontal bar chart** instead of a pie chart.  
- Displayed the **top 15 most frequent TLDs** in the dataset.  

---

### **5️⃣ HTTPS Usage Analysis**  
- Instead of a **pie chart**, analyzed HTTPS usage using an alternative visualization (`donut chart`).  
- Compared the number of URLs using HTTPS vs. non-HTTPS.  

---

### **6️⃣ Feature Scaling**  
- Applied **StandardScaler** to normalize numerical features for better model performance.  

---

### **7️⃣ Feature Selection**  
- Used **Mutual Information Score** to rank the most important features.  
- **Final Selected Features (Top 10):**  
  - `URLSimilarityIndex`  
  - `LineOfCode`  
  - `NoOfImage`  
  - `NoOfSelfRef`  
  - `NoOfCSS`  
  - `HasSocialNet`  
  - `HasCopyrightInfo`  
  - `HasDescription`  
  - **(After removing correlated features, final list updated accordingly)**  

---

### **8️⃣ Splitting Data for Model Training**  
- **Training Set:** `80%` of data  
- **Testing Set:** `20%` of data  
- Ensured stratified split to maintain class distribution.  

- **Final Data Shapes:**  
  - `X_train`: **(141,009, 10)**  
  - `X_test`: **(35,253, 10)**  
  - `y_train`: **(141,009, )**  
  - `y_test`: **(35,253, )**  

---
