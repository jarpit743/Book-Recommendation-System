# Book Recommendation System 📚

This project presents a **Book Recommendation System** that leverages two key approaches: **Popularity-Based Filtering** and **Collaborative Filtering** to suggest books based on user ratings. The system is built using Python and key machine learning libraries for recommendation systems, making it capable of recommending both general popular books and personalized book suggestions.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Techniques Used](#techniques-used)
  - [Popularity-Based Filtering](#popularity-based-filtering)
  - [Collaborative Filtering](#collaborative-filtering)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Results](#results)
- [Challenges](#challenges)
- [Future Work](#future-work)

## Overview

Book recommendation systems are widely used in online platforms like Goodreads and Amazon. They help users discover new books based on their reading history or general popularity among other readers. This project implements a book recommendation system using the **Book-Crossing dataset**, which contains user reviews and ratings for a wide range of books.

The system implements two types of recommendation engines:
- **Popularity-Based Filtering**: Suggests books that are highly rated by many users.
- **Collaborative Filtering**: Provides personalized recommendations by identifying similarities between users' preferences.


## Dataset

The system uses the **Book-Crossing dataset**, which contains:
- [Datasets Link](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- **Books**: Titles, authors, year of publication, and other metadata.
- **Users**: Demographics of the users including location and age.
- **Ratings**: Users' ratings of books on a scale from 0 to 10.

### Data Files

- `books.csv`: Contains information on book titles, authors, publication year, ISBN, etc.
- `users.csv`: Contains user data such as user ID, location, and age.
- `ratings.csv`: Contains user ratings of books.

This dataset is sourced from a publicly available dataset, which can be accessed at the following [Link](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)

## Techniques Used

### Popularity-Based Filtering

This technique recommends books that have garnered the most ratings and/or have the highest average ratings. It works well for new users with no prior ratings because it relies on the overall popularity of books.

#### Steps:
1. Count the number of ratings per book.
2. Calculate the average rating for each book.
3. Recommend books with the highest number of ratings or best average ratings.

### Collaborative Filtering

Collaborative filtering generates personalized recommendations based on user-item interactions. It leverages the concept that users who agreed on past ratings will likely agree in the future as well. This project uses **Surprise** library to implement collaborative filtering with matrix factorization.

#### Steps:
1. Create a user-item rating matrix.
2. Use collaborative filtering (e.g., **K-Nearest Neighbors** or **Matrix Factorization**) to predict ratings for books the user hasn’t interacted with yet.
3. Recommend books with the highest predicted ratings.

## Installation

Follow these instructions to set up and run the book recommendation system on your local machine:

### Clone this repository:

git clone [https://github.com/your-username/book-recommender.git](https://github.com/jarpit743/Book-Recommendation-System)
cd book-recommender
Install the required Python libraries:
pip install -r requirements.txt
Open the Jupyter notebook to run the recommendation system:
jupyter notebook BRS(Pop+Colla).ipynb

## Usage

Once the notebook is up and running, you can:

- **Explore the dataset**: Load and visualize the books, users, and ratings data.
- **Run Popularity-Based Filtering**: Generate recommendations based on book popularity.
- **Run Collaborative Filtering**: Generate personalized book recommendations for a user.

### Running the Jupyter Notebook

- Launch the notebook (`BRS(Pop+Colla).ipynb`) and execute each cell step by step.
- Visualize the recommendations in the output cells.

## Features

- **Data Visualization**: Displays insights into the dataset such as the distribution of ratings, top-rated books, and the most-rated books.
- **Popularity-Based Recommender**: A basic recommendation engine that suggests popular books.
- **Collaborative Filtering Recommender**: A personalized recommendation engine that suggests books based on user preferences.
- **Model Evaluation**: Evaluates the performance of the collaborative filtering model using cross-validation.

## Results

- **Popularity-Based Filtering**: Suggests popular books such as *'The Da Vinci Code'* and *'Harry Potter'*, which have been highly rated and read by many users.
- **Collaborative Filtering**: Provides personalized suggestions like *'The Catcher in the Rye'* or *'To Kill a Mockingbird'* based on the user's reading preferences.

### Sample output from the popularity-based recommender:
- 1. The Da Vinci Code - Dan Brown
- 2. Harry Potter and the Sorcerer's Stone - J.K. Rowling
- 3. To Kill a Mockingbird - Harper Lee

## Challenges

- Handling sparsity in the user-item matrix, as not every user has rated many books.
- Cold-start problem, where new users or new books don’t have enough data for collaborative filtering.

## Future Work

- **Hybrid Recommender**: Combining content-based filtering (using book metadata) and collaborative filtering for more accurate recommendations.
- **Web Interface**: Developing a front-end for user interaction using frameworks like Flask or Django.
- **Improved Scalability**: Optimizing the system for larger datasets and more efficient real-time recommendations.

