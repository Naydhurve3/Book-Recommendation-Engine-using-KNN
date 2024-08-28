# Book-Recommendation-Engine-using-KNN

# Project Overview
This project implements a book recommendation system using a collaborative filtering technique with k-nearest neighbors (KNN). The system is built to suggest books based on user ratings and preferences, drawing on data from the Book-Crossing dataset.

# Dataset
The project utilizes the following files from the Book-Crossing dataset:

BX-Books.csv: Contains information about books including ISBN, title, and author.
BX-Book-Ratings.csv: Contains user ratings for books identified by ISBN.
# Steps Involved
1. Data Loading and Preprocessing
Loading the Data: The dataset files are imported into Pandas DataFrames with appropriate encoding and column specifications.
Merging DataFrames: The BX-Books.csv and BX-Book-Ratings.csv files are merged on the isbn column to combine book details with user ratings.
Exploratory Data Analysis (EDA): Plots are created to visualize the distribution of the number of reviews per user and the number of reviews per book, providing insights into the data's structure.
Data Filtering: The dataset is filtered to include only books with more than 100 reviews and users with more than 200 reviews to ensure statistical significance. Duplicates in the dataset are also removed.
2. Data Transformation
Pivoting Data: The filtered dataset is rearranged into a sparse matrix format using a pivot table, where each row represents a book, each column represents a user, and the values represent the corresponding ratings. This transformation is crucial for feeding the data into the KNN model.
3. Model Building
K-Nearest Neighbors (KNN) Model: A KNN model is created using the cosine similarity metric. The model is trained on the sparse matrix created from the pivoted dataset.
4. Book Recommendation Function
get_recommends(book): This function takes a book title as input and returns a list of recommended books. The function uses the trained KNN model to find the closest matches (i.e., similar books) based on the ratings.
5. Testing
test_book_recommendation: A testing function is provided to evaluate the recommendation system. The function checks the accuracy of the recommendations against expected results.
# Conclusion
This project successfully demonstrates how to build a simple yet effective book recommendation system using collaborative filtering with KNN. The model can recommend books based on user preferences and the similarity of books in terms of user ratings.

