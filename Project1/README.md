# 🏠 Housing Price Prediction (R)

## 📌 Project Overview
This project builds a machine learning model in **R** to predict residential property prices using the **King County Housing Dataset**. The dataset contains **21,613 housing records and 21 property-related features**, including structural characteristics, location, and property condition.

The workflow includes **data preprocessing, exploratory data analysis (EDA), model training, and model evaluation** to understand the factors influencing housing prices.

---

## 📊 Dataset
- **Source:** Kaggle – King County House Sales Dataset  
- **Observations:** 21,613 houses  
- **Features:** 21 variables  

Key variables include:

- `price` – house sale price (target variable)
- `bedrooms`
- `bathrooms`
- `sqft_living`
- `sqft_lot`
- `floors`
- `waterfront`
- `view`
- `condition`
- `grade`
- `yr_built`
- `zipcode`
- `lat`, `long`

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing
- Loaded dataset using `readxl`
- Removed non-predictive features (`id`, `date`)
- Checked for missing values
- Split the dataset into **training and testing sets**

### 2️⃣ Exploratory Data Analysis
Key visualizations included:

- Housing price distribution
- Correlation analysis
- Price vs living area scatter plot
- Feature relationship analysis

These helped identify **important predictors influencing housing prices**.

---

### 3️⃣ Model Development

A **Linear Regression Model** was trained using the training dataset.

Model formula:

```
price ~ bedrooms + bathrooms + sqft_living + sqft_lot + floors + waterfront + view + condition + grade + yr_built + location features
```

The model predicts housing prices based on structural and geographic variables.

---

## 📈 Model Performance

| Metric | Value |
|------|------|
| R² | **0.82** |
| RMSE | **$161,244** |

### Interpretation
- The model explains **82% of the variance in housing prices**.
- Prediction errors increase for **very high-priced luxury homes**, which is common for linear regression models.

---

## 🔍 Key Insights

- **Living area (`sqft_living`)** is the strongest predictor of housing price.
- **Construction grade** significantly increases property value.
- Houses with **waterfront access** tend to command premium prices.
- **Location variables (`lat`, `long`, `zipcode`)** strongly influence price differences across neighborhoods.
- Larger homes generally have higher prices, though price variation increases for luxury properties.

---

## 🛠 Technologies Used

- **R**
- **RStudio**
- `tidyverse`
- `ggplot2`
- `caret`
- `randomForest`
- `readxl`
- `GGally`

---

## 📂 Project Structure

```
housing-price-prediction-r
│
├── Housing.xlsx                 # Raw housing dataset
├── House_Price_Regression.Rproj # RStudio project file
├── README.md                    # Project documentation
│
├── Dashboard.png                # Shiny dashboard preview
├── Graphs.png                   # Model and analysis visualizations
│
├── .RData                       # Saved R workspace
├── Environment Data.RData       # Environment variables and session data
```

---

## 🚀 Future Improvements

- Implement **Random Forest or Gradient Boosting models**
- Perform **feature engineering**
- Improve prediction accuracy for **high-value luxury properties**
- Expand the analysis with additional housing market data

---

## 📎 Conclusion

This project demonstrates an **end-to-end data science workflow in R**, including data exploration, predictive modeling, and model evaluation to understand key factors influencing housing prices.
