# Book Recommendation System

This project implements a **Book Recommendation System** using two different techniques: **popularity-based filtering** and **collaborative filtering**. The system suggests books to users by leveraging book ratings and interactions within the dataset.

## Project Overview

The book recommendation system is built using data on book ratings from various users, aiming to recommend books based on both popular titles and personalized suggestions for individual users. The system focuses on two main approaches:

1. **Popularity-Based Filtering:** Recommends the most popular books based on the number of ratings and average ratings received.
2. **Collaborative Filtering:** Recommends books based on the user's preferences by considering similar users' ratings.

## Dataset

The project uses the **Book-Crossing dataset**, which contains:
- Information on **books**: titles, authors, publication year, and associated metadata.
- User ratings for various books.

The dataset is available in the following format:
- [Datasets Link](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- `books.csv` contains book details such as ISBN, title, author, year of publication, and publisher.
- `ratings.csv` contains user ratings for different books.
- `users.csv` contains user demographic information.

## Features

- **Popularity-Based Recommendations**: This approach suggests books that are highly rated or frequently rated across all users.
- **Collaborative Filtering**: Utilizes the user-book interactions to recommend books based on similar users or books.

## Libraries and Tools Used

- **Python**
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib & Seaborn**: For visualizations.
- **Surprise Library**: For collaborative filtering implementation.
- **Scikit-learn**: For model building and evaluation.

## Usage

To run the recommendation system, follow these steps:

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/your-username/book-recommender.git
   cd book-recommender
