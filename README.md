# Content-Based Movie Recommender System
### Project Overview

This project implements a content-based movie recommender system that suggests movies to users based on their genre preferences.
By analyzing the genres of movies that users have previously rated, the model is able to recommend new movies they are likely to enjoy.

Unlike collaborative filtering approaches, this system does not rely on other users' preferences, making it ideal for new users or small datasets.

### Key Features

1. Data Cleaning:

    - Handled missing values and duplicates

    - Processed multi-genre movies by splitting and expanding genre fields

2. Feature Engineering:

    - One-hot encoded movie genres to create structured movie profiles

3. User Profiling:

    - Built personalized user profiles by weighting movie genres according to user ratings

4. Movie Recommendation:

    - Recommended top-N movies using cosine similarity between user profiles and movie genre profiles

5. Rating Prediction:

    - Predicted a user’s potential rating for an unseen movie based on similarity scores

### Workflow

- Load and Inspect Data

    Import ratings.csv and movies.csv, check for missing values, and understand the dataset structure.

- Data Preprocessing
    Clean the data by removing unnecessary columns (timestamp), duplicates, and movies with no listed genres.

- Feature Engineering
    Apply one-hot encoding on genres and expand multi-genre movies into multiple entries.

- User Profile Creation
    Aggregate the genres rated by each user, weighted by the user's rating, to create a preference profile.

- Recommendation Generation
    Compute cosine similarity between user profiles and movie features to recommend unseen movies.

- Rating Prediction
    Estimate how a user might rate a new movie based on the similarity between their profile and the movie’s genre composition.

### Technologies Used

- Python

- pandas

- scikit-learn (for cosine similarity)

- Jupyter Notebook

### Dataset

- ratings.csv: UserId, MovieId, Rating, Timestamp

- movies.csv: MovieId, Title, Genres

- Source: MovieLens dataset (small subset)