# 🍽️ Restaurant Analysis & Rating Prediction

## 📌 Project Overview

This project performs an exploratory data analysis and machine learning analysis on the restaurant dataset.

The project focuses on understanding restaurant characteristics such as **location, cuisine, pricing, customer votes, table booking, and online delivery**, and investigates their relationship with restaurant ratings.

Machine learning regression models are also developed to predict restaurant ratings and compare their performance.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze the distribution of restaurant ratings.
- Identify the most common cuisines and restaurant locations.
- Analyze restaurant pricing and price ranges.
- Study the availability of table booking and online delivery.
- Examine the relationship between customer votes and restaurant ratings.
- Analyze cuisine-wise and city-wise ratings.
- Identify important features influencing restaurant ratings.
- Build and compare regression models for rating prediction.

---

## 📂 Dataset

The project uses the ** restaurant dataset** containing information about restaurants, including:

- Restaurant Name
- Country Code
- City
- Address
- Locality
- Longitude
- Latitude
- Cuisines
- Average Cost for Two
- Currency
- Table Booking
- Online Delivery
- Price Range
- Aggregate Rating
- Rating Color
- Rating Text
- Votes

---

## 🛠️ Technologies Used

### Programming Language
- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Machine Learning Algorithms

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

---

# 🔍 Project Workflow

## 1. Data Loading

The dataset was loaded using Pandas and inspected to understand its structure, columns, data types, and missing values.

---

## 2. Data Cleaning

The following preprocessing steps were performed:

- Checked for missing values.
- Filled missing values in the `Cuisines` column using the mode.
- Removed the `Restaurant ID` column.
- Examined numerical and categorical variables.
- Checked the distribution of the target variable.

---

## 3. Exploratory Data Analysis

### 📊 Restaurant Rating Analysis

The distribution of `Aggregate rating` was analyzed using:

- Histograms
- Boxplots
- Frequency distributions

A large number of restaurants have a rating of `0`, representing restaurants without a recorded rating in the dataset.

---

### 🌍 Country and City Analysis

Restaurant distribution was analyzed across:

- Countries
- Cities
- Localities

Average restaurant ratings were also calculated for different cities and countries.

---

### 🍜 Cuisine Analysis

Cuisine information was analyzed to identify:

- Most common cuisines
- Cuisine-wise average ratings
- Popular cuisines based on customer votes

Since restaurants can offer multiple cuisines, the cuisine column was split and individual cuisines were analyzed separately.

---

### 💰 Price Analysis

The project analyzed:

- Average cost for two people
- Price ranges
- Average rating by price range

Visualizations were created to examine the relationship between restaurant pricing and ratings.

---

### 🪑 Table Booking & Online Delivery

The availability of restaurant services was analyzed.

The percentage of restaurants offering:

- Table booking
- Online delivery

was calculated.

The relationship between these services and restaurant ratings was also explored.

---

### ⭐ Rating vs Customer Votes

The relationship between customer votes and restaurant ratings was visualized using a scatter plot.

The analysis showed a strong association between customer votes and the rating prediction model.

---

# 🧮 Feature Engineering

Two additional features were created:

```python
df['Restaurant Name Length'] = df['Restaurant Name'].astype(str).str.len()

df['Address Length'] = df['Address'].astype(str).str.len()
```
---

# 🤖 Machine Learning

The target variable was:

Aggregate rating

The dataset was divided into:

80% Training Data
20% Testing Data

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)

Three regression models were evaluated.
```
---

# 📈 Model Performance
Model	R² Score	MAE	RMSE
Linear Regression	0.3056	1.046	1.257
Decision Tree	0.9216	0.274	0.422
Random Forest	0.9629	0.190	0.290

Evaluation Metrics

R² Score

Measures how much of the variation in restaurant ratings is explained by the model.

MAE (Mean Absolute Error)

Measures the average absolute difference between actual and predicted ratings.

RMSE (Root Mean Squared Error)

Measures prediction error while giving greater weight to larger errors.

# 🌲 Feature Importance

Feature importance was analyzed using the Random Forest model.

The most important features included:

Feature	Importance
Votes	0.9457
Longitude	0.0131
Latitude	0.0098
Cuisines	0.0083
Address Length	0.0057
Average Cost for Two	0.0055
Restaurant Name Length	0.0045

The Votes feature had the highest importance in the Random Forest model.

This indicates that customer engagement represented by votes has a strong association with the predicted restaurant rating in this dataset.

# 📊 Key Findings
Restaurant ratings are not uniformly distributed.
A substantial number of restaurants have a rating of 0.
Restaurants are distributed unevenly across cities and countries.
Cuisine preferences vary considerably across locations.
Restaurant pricing varies across different price ranges.
Table booking and online delivery are available only for a subset of restaurants.
Customer votes show a strong relationship with restaurant ratings.
Tree-based models performed substantially better than Linear Regression on the test dataset.
Random Forest achieved an R² score of 0.9629.
Votes was the dominant feature in the Random Forest model.

# 📝 Conclusion

This project combines exploratory data analysis with machine learning to understand restaurant characteristics and predict restaurant ratings.

Three regression models were evaluated:

Linear Regression
Decision Tree Regressor
Random Forest Regressor

Among the evaluated models, Random Forest achieved the highest test-set R² score and the lowest MAE and RMSE.

The analysis also highlighted the importance of customer votes in the prediction of restaurant ratings.

The project demonstrates the complete data science workflow, including data cleaning, exploratory data analysis, feature engineering, visualization, machine learning, model evaluation, and feature importance analysis.

# ⚠️ Limitations
The dataset contains a considerable number of restaurants with a rating of 0.
The Random Forest model relies heavily on the Votes feature.
Categorical variables were encoded numerically for the machine learning models.
The analysis identifies relationships in the dataset but does not establish causal relationships.
Model performance is specific to the available dataset and train-test split.

# 📁 Project Structure
Restaurant-Analysis/
│
├── Restaurant_Analysis.ipynb
├── Dataset.csv
├── README.md
└── images/
    └── visualizations/
    
# 🚀 How to Run the Project
1. Clone the repository
git clone <your-github-repository-url>
2. Navigate to the project directory
cd Restaurant-Analysis
3. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn
4. Launch Jupyter Notebook
jupyter notebook

Open the project notebook and run the cells sequentially.

# 👩‍💻 Skills Demonstrated
Python
Data Cleaning
Exploratory Data Analysis
Data Visualization
Feature Engineering
Statistical Analysis
Regression
Model Evaluation
Feature Importance
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn

# ⭐ Project Highlights

Dataset: Restaurant Dataset
Task: Restaurant Rating Prediction
Problem Type: Regression
Best Test R²: 0.9629
Best Test MAE: 0.190
Best Test RMSE: 0.290
Best Performing Model: Random Forest Regressor

# 📌 Author

Apeetha Srinivasan

Data Science | Machine Learning | Python
