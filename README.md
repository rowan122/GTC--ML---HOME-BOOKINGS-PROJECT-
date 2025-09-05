# 🏨 Hotel Booking Analysis

**Short Description:** Exploratory data analysis and preprocessing of hotel booking data to understand customer behavior, cancellations, and booking patterns. Includes data cleaning, feature engineering, and train/test split to prepare for ML.

## 📂 Dataset
The dataset used in this project is the **Hotel Booking Demand Dataset**, available on [Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) and originally published in [Data in Brief](https://www.sciencedirect.com/science/article/pii/S2352340918315191).  
It contains information on hotel reservations including booking cancellations, customer demographics, and stay details.

## 📊 Workflow
1) **EDA**
- Inspect shape/dtypes/stats
- Missing values & duplicates check

2) **Cleaning**
- Fill NAs: `company`, `agent`, `country`, `children`
- Remove duplicates (**32,013** rows)

3) **Feature Engineering**
- `total_guests = adults + children + babies`
- `total_nights = stays_in_week_nights + stays_in_weekend_nights`
- `is_family` flag
- `country_freq` (frequency encoding)

4) **Prep for Modeling**
- Drop: `reservation_status`, `reservation_status_date`
- Encode categoricals & scale numerics (as needed)
- Train/test split:
  - `X_train: (69,901, 33)`
  - `X_test: (17,476, 33)`

## 🛠 Tech
- Python: pandas, numpy
- Viz: matplotlib, seaborn
- Scikit-learn (preprocessing, split)

## 📸 Sample Visualization
Example of EDA visualization (distribution of cancellations):

![sample chart](path/to/chart.png)

## 🚀 Next
- Train models (LogReg, RandomForest, …) to predict `is_canceled`
- Evaluate: accuracy, precision, recall, ROC-AUC
