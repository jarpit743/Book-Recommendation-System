# Book Recommendation System

## Overview
This project is a **Book Recommendation System** that recommends books based on popularity and collaborative filtering. It utilizes a dataset of users, books, and their ratings to build two types of recommendation systems:
- **Popularity-Based Recommender**: Recommends books based on the number of ratings and the average rating.
- **Collaborative Filtering Recommender**: Suggests books based on similar user preferences.

## Dataset
- [Datasets Link](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- **Books Dataset**: Contains information about books such as title, author, publication year, and cover images.
- **Users Dataset**: Contains user demographic information like location and age.
- **Ratings Dataset**: Contains user ratings of books on a scale of 0 to 10.

## Libraries Used
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical computations.
- **scikit-learn**: For calculating cosine similarity in collaborative filtering.
- **Flask**: For building the web application.
- **pickle**: For saving and loading models and data structures.

## Features
1. **Popularity-Based Recommender**:
   - Displays top books based on the number of ratings and average rating.
   - Filters out books that have received less than 250 ratings.

2. **Collaborative Filtering Recommender**:
   - Uses user-item interaction matrix and cosine similarity to find similar books.
   - Provides personalized recommendations based on a selected book.

## Files
- `app.py`: Flask web application that serves the recommendation system.
- `books.csv`: Contains book metadata.
- `users.csv`: Contains user metadata.
- `ratings.csv`: Contains user ratings for books.
- `popular.pkl`: Preprocessed data for the popularity-based recommender.
- `pt.pkl`: Pivot table for collaborative filtering.
- `similarity_scores.pkl`: Cosine similarity scores for collaborative filtering.
- `books.pkl`: Preprocessed book data.
- `templates/index.html`: HTML file for displaying the popular books.
- `templates/recommend.html`: HTML file for displaying book recommendations.

## How to Run
1. Clone the repository and install the required libraries:
    ```bash
    git clone https://github.com/your-username/book-recommendation-system.git
    cd book-recommendation-system
    pip install -r requirements.txt
    ```

2. Run the Flask app:
    ```bash
    python app.py
    ```

3. Access the web app at `http://127.0.0.1:5000/` to use the book recommendation system.

## Usage
- The homepage displays the most popular books based on the number of ratings and average rating.
- Navigate to the recommendation page and input a book name to get personalized recommendations based on collaborative filtering.

## Example
- Recommending books similar to "1984":
    - **Animal Farm**
    - **The Handmaid's Tale**
    - **Brave New World**
    - **The Vampire Lestat (Vampire Chronicles, Book II)**

## Future Enhancements
- Add more recommendation algorithms like content-based filtering.
- Implement user login and personalized recommendations based on user history.

## License
This project is licensed under the MIT License.
