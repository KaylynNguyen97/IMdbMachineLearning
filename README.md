# Film Forecast: Predicting IMDb Ratings with Machine Learning

## Executive Summary

This project developed a machine learning model to predict IMDb movie ratings. We analyzed movie characteristics and compared three models: Random Forest, CatBoost, and LightGBM. Our analysis identified key factors influencing ratings and demonstrated machine learning's potential in predicting audience reception.

**CatBoost** was the best-performing model, achieving the lowest RMSE (\$0.8236\$) and highest R² score (\$0.5049\$). Influential features included the number of voted users, genres, and movie duration. This model has applications in box office prediction, marketing, and production decisions.

## Project Overview

The entertainment industry increasingly relies on data-driven decisions. IMDb scores are crucial for movie success. With over 500 US movie releases annually, accurately predicting audience reception offers valuable insights for filmmakers and marketers. This project aims to develop a predictive model using machine learning to analyze movie characteristics (genre, duration, audience engagement) and anticipate IMDb ratings more accurately, supporting informed decision-making.

## Methodology

Our project followed these steps:

1.  **Data Preparation:** Cleaned and split the Kaggle IMDb Movie Ratings Dataset.
2.  **Model Selection:** Employed and compared Random Forest, CatBoost, and LightGBM.
3.  **Exploratory Data Analysis (EDA):** Analyzed feature impact on IMDb scores.
4.  **Cold-Start Problem:** Addressed pre-release (cast, director, genre) and post-release (votes, reviews) factors.
5.  **Model Building:** Built the IMDb Score Prediction model using the optimal choice.

## Key Findings

### Model Performance
CatBoost outperformed other models in predicting IMDb ratings:

| Model          | RMSE    | R² Score |
| :------------- | :------ | :------- |
| **CatBoost**   | **0.8236** | **0.5049** |
| LightGBM       | 0.8440  | 0.4799   |
| Random Forest  | 0.8607  | 0.4592   |

CatBoost's strengths include handling categorical features, sparse data, and built-in regularization.

### Feature Importance
-   **Most Important:** Number of voted users.
-   **Other Significant Features:** Genres, movie duration, and release year.
-   **Genre Impact:** Informational genres (film noir, news, documentary) tend to have higher average ratings, while horror, reality TV, and game shows have lower ratings.
-   **Audience Engagement:** Positive relationship between number of votes and average IMDb scores.
-   **Movie Duration:** Movies under one hour or over three hours tend to have higher average ratings.
-   **Temporal Trends:** Older movies (pre-1980) tend to have higher average ratings; recent movies show more polarizing reception.

### IMDb Score Prediction Model
To address the "cold-start problem" for new movies, we propose a **two-model approach**:
-   **Pre-release Model:** Uses director, cast, and genre to forecast ratings.
-   **Post-release Model:** Incorporates audience metrics (votes, reviews) after release to refine predictions.

## Recommendations

-   **Use CatBoost:** For its superior performance and ability to handle complex feature interactions.
-   **Feature Engineering:** Focus on audience engagement, genre classification, historical performance of directors/actors, and temporal trends.
-   **Two-Model Approach:** Implement separate models for pre-release and post-release predictions.
-   **Genre-Specific Models:** Consider developing models tailored to specific movie genres.
-   **Prioritize User Data:** Emphasize features related to user votes and reviews.

## Conclusion

Our machine learning approach effectively predicts IMDb ratings, offering valuable insights for the film industry. CatBoost emerged as the best-performing model, capable of informing box office predictions, marketing strategies, and production decisions. By addressing the cold-start problem and incorporating robust feature engineering, this project provides a powerful tool for understanding audience perception and movie quality.
