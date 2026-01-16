# Corporate Credit Rating Classification

## 📌 Project Overview
This project focuses on classifying corporate credit ratings based on financial indicators. It explores and compares the performance of **Machine Learning (Random Forest)** and **Deep Learning (Deep Neural Network)** models to determine the most effective approach for multiclass classification tasks involving imbalanced data.

## 🎯 Objectives
* To classify corporate credit ratings using a set of financial ratios and indicators.
* To compare the accuracy and robustness of Machine Learning vs. Deep Learning models.
* To address and mitigate the issue of **class imbalance** in the dataset.

## 📊 Dataset
The dataset is sourced from **Kaggle's Corporate Credit Rating** data.
* **Size:** 2,029 entries.
* **Features:** 30 columns, including 25 key financial indicators categorized into:
    * **Liquidity Measurement:** Current Ratio, Quick Ratio, Cash Ratio, Days of Sales Outstanding.
    * **Profitability Indicators:** Gross Profit Margin, Operating Profit Margin, Net Profit Margin, ROA, ROE, ROCE.
    * **Debt Ratios:** Debt Ratio, Debt-to-Equity Ratio.
    * **Operating Performance:** Asset Turnover.
    * **Cash Flow Indicators:** Operating Cash Flow per Share, Free Cash Flow per Share.

## ⚙️ Methodology

### 1. Data Preprocessing
* Data cleaning and feature selection.
* Exploratory Data Analysis (EDA) to understand feature distributions.

### 2. Handling Imbalanced Data
Since credit rating datasets are often imbalanced (few companies have extremely high or low ratings), the project applies specific techniques to improve model performance:
* **SMOTE + ENN (Synthetic Minority Over-sampling Technique + Edited Nearest Neighbours):** Used to synthesize minority class samples and clean noisy data.
* **Class Weighting:** Assigning higher weights to minority classes during model training.

### 3. Model Development
The following models were developed and evaluated:
* **Random Forest (Base Model)**
* **Random Forest + SMOTE & ENN**
* **Random Forest + Class Weights**
* **Deep Neural Network (DNN)**

## 📈 Results & Conclusion
* **Deep Learning (DNN):** The DNN model showed limitations in this specific task, particularly with minority classes (e.g., the 'Unrank' class), achieving a Recall of 0. This suggests that the dataset size might be insufficient for training a robust deep learning architecture without further augmentation or tuning.
* **Random Forest:** The **Random Forest model combined with SMOTE+ENN** and the **Weighted Class Random Forest** achieved the highest accuracy. These models demonstrated superior ability to handle the multiclass imbalance, making them the most suitable solution for this dataset.

<img width="903" height="409" alt="image" src="https://github.com/user-attachments/assets/33dae437-2f3b-4c32-ac6a-81b944f7fcf1" />


## 🛠 Tools & Technologies
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn
* **Deep Learning:** TensorFlow / Keras
