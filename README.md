# RESM(Restaurant-Evaluation-and-Success-Model)
A predictive model to assess the likelihood of restaurant closure within the next 4 years. Built to assist lenders and investors in making informed decisions, the model leverages machine learning on data from multiple sources.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Machine Learning Approach](#machine-learning-approach)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

## Overview
This project aims to predict whether a restaurant is likely to close within a 4-year period by analyzing historical and current data. We compiled a dataset from Yelp and Google APIs, then performed feature engineering to enhance prediction accuracy.

### Key Objectives
1. Build a dataset of historical and current restaurant information.
2. Develop a logistic regression model to assess closure risk.
3. Create an interactive dashboard for data visualization and insights.

## Features
- **Data Compilation**: Aggregates data from Yelp Search API and Google Search API.
- **Data Matching**: Ensures consistency between historical and current datasets.
- **Feature Engineering**: Enhances data for improved predictive accuracy.
- **Predictive Model**: Logistic Regression and Gradient Boosting models.
- **Interactive Dashboard**: Built with Streamlit to visualize insights.

## Tech Stack
- **Languages**: Python
- **APIs**: Yelp Search API, Yelp Business API, Google Custom Search API
- **Libraries**: Pandas, NumPy, Scikit-learn, Streamlit
- **Environment**: Jupyter Notebooks

## Machine Learning Approach

### 1. Data Collection and Preparation
The model relies on a dataset sourced from Yelp and Google APIs, which provides data on historical and current restaurant statuses. Data collected includes factors such as location, review ratings, price category, and restaurant type, which may influence the likelihood of restaurant closure.

### 2. Feature Engineering
Feature engineering is critical to improving model accuracy by transforming raw data into meaningful attributes. In this project, features engineered include:
- **Business attributes**: Ratings, price levels, number of reviews, etc.
- **Location data**: Factors such as city and neighborhood population density, income levels, and nearby competition.
- **Temporal data**: Yearly and seasonal trends, considering the time period for business closures and openings.

### 3. Model Selection
Multiple machine learning models were evaluated to determine the best fit for predicting restaurant closures:
- **Logistic Regression**: This model was chosen as the primary classifier due to its simplicity and interpretability. It performs well with binary classification tasks like predicting closure risk.
- **Gradient Boosting**: Used to improve model performance, this method enhances prediction accuracy by combining multiple weak learners into a single strong learner.

### 4. Model Training and Optimization
Using **Scikit-learn**, the logistic regression and gradient boosting models were trained on the dataset with optimized hyperparameters. Cross-validation was performed to assess model generalizability and prevent overfitting. Key performance metrics used in evaluation include:
- **Accuracy**: The percentage of correct predictions.
- **Precision and Recall**: To measure the model's ability to correctly predict closures.
- **F1 Score**: The harmonic mean of precision and recall, useful for imbalanced datasets.

### 5. Dashboard for Insights
An interactive dashboard, built with **Streamlit**, allows users to visualize model predictions, explore feature impacts, and filter data. This enables lenders and investors to gain insights into the factors affecting restaurant success.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/s11saurabh/RESM-Restaurant-Evaluation-and-Success-Model-
   cdRESM-Restaurant-Evaluation-and-Success-Model-
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up API keys for Yelp and Google Custom Search:
   - Add your API keys in a `.env` file:
     ```
     YELP_API_KEY=your_yelp_api_key
     GOOGLE_API_KEY=your_google_api_key
     ```

## Usage

1. Run the notebooks in sequence to build and clean the dataset, engineer features, and train models.
2. Start the Streamlit dashboard:
   ```bash
   streamlit run dashboard.py
   ```
3. Open the dashboard in your browser to explore predictions and insights.

## Project Structure

```plaintext
.
├── data/
│   ├── raw/                   # Raw data files
│   └── processed/             # Processed data after feature engineering
├── notebooks/
│   ├── Restaurants_yelp_GoogleCustomSearchAPI.ipynb
│   ├── Restaurants_yelp_API_for_GoogleSearchResults.ipynb
│   ├── Restaurants_yelp_join_all.ipynb
│   ├── Restaurants_yelp_more_features_final.ipynb
│   └── Restaurants_yelp_ML_final.ipynb
├── dashboard.py               # Streamlit dashboard code
├── README.md
└── requirements.txt
```

## Results
The logistic regression and gradient boosting models demonstrated strong predictive capability in identifying closure risks. Insights into key factors influencing closures are visualized on the Streamlit dashboard. For further details, refer to our [blog post](link-to-blog-post).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
