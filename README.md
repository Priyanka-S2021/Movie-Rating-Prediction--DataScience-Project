# 🎬 IMDb Indian Movies Rating Prediction

## 📌 Overview

This project aims to predict IMDb ratings for Indian movies using a combination of data preprocessing, feature engineering, and machine learning models. By leveraging technique like Random Forest  the model provides insights into factors influencing movie ratings.

## 📂 Dataset Source: Kaggle (https://www.kaggle.com/datasets/adrianmcmahon/imdb-india-movies)
- **Dataset**: IMDb India Movies
- **Features**:
  - Name
  - Year
  - Genre
  - Rating
  - Votes
  - Director
  - Actor 1
  - Actor 2
  - Actor 3
## 🛠️ Project Workflow

### 1. Data Preprocessing

- Dropped columns with more than 50% missing values.
- Removed the 'Duration' column due to inconsistencies.
- Stripped whitespace from column names.
- Handled missing values by filling with zeros.
- Normalized the 'Genre' column to lowercase.
- Identified and removed outliers in the 'Rating' column using the IQR method.

### 2. Exploratory Data Analysis (EDA)

- Visualized the distribution of ratings using boxplots.
- Generated an automated EDA report using Sweetviz.
  
### 3. Feature Engineering

- Calculated 'movie_age' as the difference between 2025 and the release year.
- Created a binary feature 'is_old_movie' for movies released before 2000.
- Computed average ratings per genre and director.
- Assessed actor popularity based on average votes.
- Formed actor combinations and evaluated their popularity.
- Introduced flags for missing director and actor information.

### 4. Data Transformation

- Imputed missing numerical values with the mean.
- Imputed missing categorical values with the mode.
- Encoded binary categorical variables using LabelEncoder.
- Scaled numerical features using StandardScaler.

### 5. Model Training and Evaluation

- **Models Comparison**:
-  **Linear Regression**:
  - MAE: 0.378
  - RMSE: 0.551
  - R² Score: 0.691
- **Random Forest**:
  - MAE: 0.136
  - RMSE: 0.259
  - R² Score: 0.932
- **XGBoost**:
  - MAE: 0.141
  - RMSE: 0.259
  - R² Score: 0.932
  
  ### Model Used: - Random Forest Regressor
 
- **Performance Metrics**:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score 
### 6. Hyperparameter Tuning

- Performed RandomizedSearchCV on Random Forest to optimize parameters.

### 7. Model Interpretation

- Analyzed feature importance using SHAP values.
- Visualized partial dependence plots for key features. 
## 📈 Results

- **Tuned Random Forest**:
  - MAE: 0.137
  - RMSE: 0.252
  - R² Score: 0.936 
## 📊 Visualizations

- Boxplots for rating distribution.
- Histograms for numerical feature distributions.
- Feature importance bar chart and SHAP summary
  
## 🧰 Tools and Libraries

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn
- XGBoost
- SHAP
- Sweetviz
 
