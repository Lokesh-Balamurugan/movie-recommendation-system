# Movie Recommendation System

A sophisticated system designed to offer personalized movie suggestions tailored to individual user preferences using advanced data analysis and machine learning algorithms.

## Table of Contents
- [Description](#description)
- [Installation](#installation)
- [Features](#features)
- [Results](#results)
- [Streamlit Application](#streamlit-application)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Description

In a world where movies serve as a universal medium of entertainment, catering to a diverse range of tastes and preferences, the role of a finely tuned recommendation system becomes essential. This "Movie Recommendation System" is designed to predict and suggest movies that align with a user's preferences by analyzing their past movie-watching habits. The system is trained with both Memory-Based Collaborative Filtering and Model-Based Collaborative Filtering techniques, which we will compare to see which performs better to provide the best recommendations.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/username/movie-recommendation-system.git
    cd movie-recommendation-system
    ```

2. Download the dataset:
    - [MovieLens 25M Dataset](https://www.kaggle.com/datasets/patriciabrezeanu/movielens-full-25-million-recommendation-data)

3. Place the dataset files in the appropriate directory:
    ```plaintext
    movie-recommendation-system/
    ├── data/
    │   ├── genome-scores.csv
    │   ├── genome-tags.csv
    │   ├── links.csv
    │   ├── movies.csv
    │   ├── ratings.csv
    │   └── tags.csv
    ```

## Features

- **Memory-Based Collaborative Filtering**:
  - User-Based Collaborative Filtering: Identifies users with similar preferences and recommends movies they liked.
  - Item-Based Collaborative Filtering: Recommends movies similar to those the user has liked in the past.

- **Model-Based Collaborative Filtering**:
  - Singular Value Decomposition (SVD): Decomposes the user-item interaction matrix to predict ratings.
  - Non-negative Matrix Factorization (NMF): Factors the matrix into non-negative matrices to predict ratings.
  - CoClustering: Simultaneously clusters rows and columns of the user-item matrix.
  - SlopeOne: A simple yet effective collaborative filtering algorithm.
  - Neural Networks: Utilizes dense vectors for users and items to predict ratings using complex patterns.

## Results

The analysis compared various collaborative filtering techniques and their effectiveness in predicting user preferences. The RMSE (Root Mean Square Error) was used as the evaluation metric. Here are the results:

- **Singular Value Decomposition (SVD)**: RMSE of 0.7637
- **Non-negative Matrix Factorization (NMF)**: RMSE of 1.1196
- **CoClustering**: RMSE of 0.8721
- **SlopeOne**: RMSE of 0.8325
- **Neural Networks**: RMSE of 0.7649
- **Memory-Based User Collaborative Filtering**: RMSE of 1.3739
- **Memory-Based Item Collaborative Filtering**: RMSE of 2.5031

The **Neural Network** model emerged as the most effective, delivering precise predictions consistently and demonstrating a robust capability to capture complex user-movie interactions. The **SVD** model also performed well, offering a good balance of efficiency and interpretability.

## Streamlit Application

Even though we can't create users with their favorite movies and preferences dynamically, we have a dataset with different user IDs and their favorite movies. The application uses this dataset, where users can enter a user ID and receive movie recommendations.

You can access the application here: [Movie Recommendation App](https://huggingface.co/spaces/lokeshbalamurugan20/MovieRecommendation).

## Contributing

Absolyely love contributions to improve this movie recommendation system! Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
