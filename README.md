# 🏠 House Price Prediction

## 📌 Project Overview
This project aims to predict house prices using various machine-learning regression models. By leveraging different algorithms, we compare their performance based on Root Mean Squared Error (RMSE) values and determine the most effective model for accurate predictions. 

## 📊 Dataset
The dataset contains various features related to house properties, including:
- **Square Footage**
- **Number of Bedrooms and Bathrooms**
- **Location Factors**
- **Year Built**
- **Lot Size**
- **Nearby Amenities**
- **Market Trends**

## 🛠 Models Used
We implemented and compared multiple regression algorithms to analyze their predictive power:

- **Linear Regression (LR)** – A simple baseline model for prediction.
- **K-Nearest Neighbors (KNN)** – A non-parametric approach that averages the nearest neighbors.
- **Decision Tree (CART)** – A tree-based model that makes decisions based on feature splits.
- **Random Forest (RF)** – An ensemble method combining multiple decision trees.
- **Gradient Boosting (GBM)** – A boosting algorithm that improves weak learners.
- **XGBoost** – An optimized gradient boosting technique.
- **LightGBM** – A high-performance gradient boosting model optimized for large datasets.

## 📊 Model Performance (RMSE Values)
| Model | RMSE |
|--------|------------|
| **Linear Regression** | 52588.3054 |
| **KNN** | 50620.09 |
| **CART** | 40931.5896 |
| **Random Forest** | 31281.5472 |
| **GBM** | 27111.0259 |
| **XGBoost** | 29082.8707 |
| **LightGBM** | 30631.9594 |

## ⚙️ Installation and Setup
### Step 1: Install Required Libraries
Ensure you have Python installed, then install the necessary dependencies:
```bash
pip install numpy pandas scikit-learn lightgbm xgboost matplotlib seaborn
```

### Step 2: Clone the Repository
```bash
git clone https://github.com/faiggafarov/house-price-prediction.git
cd house-price-prediction
```

### Step 3: Run the Prediction Script
Execute the Python script to train models and predict house prices:
```bash
python house_price_prediction.py
```

## 📈 Data Preprocessing Steps
Before training the models, the dataset undergoes the following preprocessing steps:
1. **Handling Missing Values** – Impute or drop missing values.
2. **Feature Encoding** – Convert categorical variables into numerical representations.
3. **Feature Scaling** – Standardize numerical features to improve model performance.
4. **Train-Test Split** – Split data into training and testing sets.

## Feature Selection
To enhance model accuracy, a feature importance analysis was conducted. The most relevant features influencing house prices were selected to optimize prediction performance.

## Evaluation Metrics
The models are evaluated using **Root Mean Squared Error (RMSE)**, a common metric for regression tasks. RMSE measures the model's predictive accuracy, with lower values indicating better performance.

## 🚀 Future Improvements
- Implementing **Hyperparameter Tuning** to optimize model performance.
- Adding **Deep Learning Models** (e.g., Neural Networks) for comparison.
- Integrating real-world **Web Scraped Data** for dynamic price predictions.
- Deploying the model as a **Web Application** for user-friendly interaction.

📌 **For more details, check the official documentation:** [LightGBM Documentation](https://lightgbm.readthedocs.io/)
