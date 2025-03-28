# Coin Catalyst

## 📈 Project Overview

This project aims to predict cryptocurrencies price trends using various machine learning models. The objective is to analyze the historical price of Cryptocurrencies and predict whether buying Cryptocurrencies at a given point would be profitable or not.

We achieve this by analyzing OHLC (Open, High, Low, Close) data and performing extensive exploratory data analysis (EDA), feature engineering, and model evaluation to predict future price movements.

---

## 🛠️ Libraries and Tools Used

- **Pandas:** For data manipulation and analysis.
- **NumPy:** To perform fast and efficient numerical operations.
- **Matplotlib/Seaborn:** For data visualization and understanding trends.
- **Scikit-learn (Sklearn):** For preprocessing, model building, and evaluation.
- **XGBoost:** An optimized gradient boosting algorithm for higher accuracy.

---

## 📚 Dataset Information

The dataset contains OHLC data of Cryptocurrencies from **July 17, 2014** to **December 29, 2022**. It consists of 2713 rows and 7 columns representing:

- **Date:** The date of the transaction.
- **Open:** Opening price of Cryptocurrencies.
- **High:** Highest price of Cryptocurrencies during the day.
- **Low:** Lowest price of Cryptocurrencies during the day.
- **Close:** Closing price of Cryptocurrencies.
- **Adj Close:** Adjusted closing price.
- **Volume:** Volume of transactions.

⚠️ Note: The **`Adj Close`** column was dropped due to redundancy.

---

## 🔎 Exploratory Data Analysis (EDA)

### Key Observations:
- Visualization of Cryptocurrencies closing prices shows an upward trend.
- Distribution and boxplots reveal outliers, indicating sudden price spikes.
- Feature engineering derived new columns like `year`, `month`, and `day` for better trend analysis.
- Additional columns created:
  - **open-close:** Difference between opening and closing prices.
  - **low-high:** Difference between lowest and highest prices.
  - **is_quarter_end:** Indicator if the date is a quarter-end.

### Data Cleaning:
- Checked for null values (none found).
- Checked for correlation using a heatmap to avoid multi-collinearity.

---

## 🧠 Feature Engineering

New features were engineered to enhance model performance:

- **Year, Month, Day:** Extracted from the `Date` column.
- **open-close:** Indicator of price movement.
- **low-high:** Reflects price fluctuations.
- **is_quarter_end:** Helps capture quarterly price trends.

These features contributed to training more robust machine learning models.

---

## 🎯 Model Development and Evaluation

### Models Used:
1. **Logistic Regression:** Basic classification model.
2. **Support Vector Classifier (SVC):** Applied with polynomial kernel.
3. **XGBoost Classifier:** Advanced gradient boosting technique.
---

## 📊 Evaluation Metrics
- **ROC-AUC Curve:** Used for measuring the accuracy of soft probability predictions.
- **Confusion Matrix:** Visualized for model evaluation.

### Final Observations:
- XGBoost showed the highest training accuracy but suffered from overfitting.
- Logistic Regression had a more balanced performance and was less prone to overfitting.

---

## 📝 Usage

### 1. Clone the Repository:
```bash
git clone https://github.com/your-repo-name.git
cd Cryptocurrencies-price-prediction
