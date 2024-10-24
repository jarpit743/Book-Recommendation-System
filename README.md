# Book Recommendation System 📚

This project presents a **Book Recommendation System** that leverages two key approaches: **Popularity-Based Filtering** and **Collaborative Filtering** to suggest books based on user ratings. The system is built using Python and key machine learning libraries for recommendation systems, making it capable of recommending both general popular books and personalized book suggestions.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
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
- [Acknowledgments](#acknowledgments)
- [Contributing](#contributing)
- [License](#license)

## Overview

Book recommendation systems are widely used in online platforms like Goodreads and Amazon. They help users discover new books based on their reading history or general popularity among other readers. This project implements a book recommendation system using the **Book-Crossing dataset**, which contains user reviews and ratings for a wide range of books.

The system implements two types of recommendation engines:
- **Popularity-Based Filtering**: Suggests books that are highly rated by many users.
- **Collaborative Filtering**: Provides personalized recommendations by identifying similarities between users' preferences.

## Project Structure

The project files are structured as follows:

bash
├── data/
│   ├── books.csv          # Contains book metadata
│   ├── ratings.csv        # Contains user ratings for books
│   └── users.csv          # Contains user demographic information
├── BRS(Pop+Colla).ipynb   # Jupyter notebook with the entire code for the recommender system
├── README.md              # Project README file
├── requirements.txt       # List of Python dependencies
└── images/                # Folder for storing images or plots generated during analysis

## Dataset

The system uses the **Book-Crossing dataset**, which contains:

- **Books**: Titles, authors, year of publication, and other metadata.
- **Users**: Demographics of the users including location and age.
- **Ratings**: Users' ratings of books on a scale from 0 to 10.

### Data Files

- `books.csv`: Contains information on book titles, authors, publication year, ISBN, etc.
- `users.csv`: Contains user data such as user ID, location, and age.
- `ratings.csv`: Contains user ratings of books.

This dataset is sourced from a publicly available dataset, which can be accessed at the following [link](http://www2.informatik.uni-freiburg.de/~cziegler/BX/).

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

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/book-recommender.git
   cd book-recommender
