# <b>Collaborative Filtering Based Recommendation System</b>

## <b><u>Dataset</u></b>

<b><a href="https://grouplens.org/datasets/movielens/latest/" style="font-size:15px;">Grouplens Movie Dataset</a></b>

The first dataset(movies.csv) contains the following features:-

- movieId - A unique identifier for each movie.
- title - The title of the movie.
- genres - The genre of the movie, Action, Comedy ,Thriller etc.

The second dataset(ratings.csv) has the following features:-

- userId - A unique identifier for each user who has given a rating for a particular movie.
- movieId - A unique identifier for each movie.
- rating - The rating provided by the user for a movie(out of 5)
- timestamp - The time when the rating was provided

## <b><u>Using Ratings and Rating Count for a Movie</u></b>
1. Converting dataset into a pivot table using the columns 'title' and 'userId'.This creates dataframe with the columns as the movie titles and row indexes as user ids in which the values as the rating provided by that user for that movie(NaN if no rating given).
2. We find the similar movies by using Correlation with the selected movie.
3. We only consider those similar movies which have more than 100 ratings and then filter them on basis of their ratings in descending order.
4. Displaying the top 10 movies.


## <b><u>Using KNN</u></b>
1. Converting dataset into a pivot table using the columns 'title' and 'userId'.This creates dataframe with the columns as the userIds and row indexes as movie titles in which the values as the rating provided by that user for that movie(0 if no rating given).
2. Scipy's csr_matrix - to convert pivot table into a sparse matrix.
3. Sklearn's NearestNeighbors -using the KNN Machine Learning Model to find the nearest movies for the selected movie based on the distance between the movies.
4. Displaying the top 5 movies.