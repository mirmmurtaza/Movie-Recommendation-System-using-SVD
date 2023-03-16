# Movie Recommendation System using SVD
This project aims to create a movie recommendation system using the Singular Value Decomposition (SVD) algorithm. The dataset used for this project is the MovieLens dataset, which consists of movie ratings provided by users.

## Overview
The recommendation system predicts users' movie ratings based on their past behavior and the behavior of similar users. The system employs collaborative filtering, a technique that leverages user-item interactions to recommend items that are likely to interest the user. In this project, I used the SVD algorithm from the Surprise library, a popular Python library for building and analyzing recommendation systems.

## Data
The MovieLens dataset consists of two main files:

**ratings.csv**: Contains user-movie interactions, including user IDs, movie IDs, and the corresponding ratings.
**movies.csv**: Contains movie metadata, such as movie IDs, titles, and genres.
In this project, I primarily use the ratings.csv file to build the recommendation system.

## Methodology
- Load the MovieLens dataset and create a Reader object with the appropriate rating scale.
- Load the dataset into a Surprise Dataset object using Dataset.load_from_df().
- Split the data into train and test sets using train_test_split().
- Perform grid search with cross-validation using the GridSearchCV class to find the best hyperparameters for the SVD model.
- Train the SVD model using the best hyperparameters on the trainset.
- Make predictions on the test set and compute evaluation metrics (RMSE and MAE).

##Results
The SVD-based recommendation system is evaluated using the root mean square error (RMSE) and mean absolute error (MAE) metrics. The model's performance can be further improved by fine-tuning the hyperparameters or trying other algorithms.

