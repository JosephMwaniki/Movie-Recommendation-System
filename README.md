# Movie Recommendations

**Author**: Joseph Mureithi Mwaniki

## Overview

The project aims to enhance Fmovies' movie streaming experience by creating a sophisticated recommendation system. Fmovies, a startup in the streaming industry, seeks to compete with major players like Netflix. The recommendation system's importance is highlighted by the fact that over 80% of shows watched on Netflix are influenced by their recommendations. The goal is to make it easy for Fmovies' users to discover their next favorite movie, ultimately increasing customer satisfaction and loyalty. This project is expected to elevate Fmovies' position in the streaming industry and redefine how users engage with movies on the platform.


## Business Understanding 
Fmovies, a burgeoning player in the movie streaming industry, faces the formidable challenge of competing with established giants like Netflix, Hulu, and Amazon Prime. In order to thrive in this rapidly expanding global market, Fmovies, our stakeholder, has identified the urgent need for an advanced movie recommendation system for their platform.

The existing landscape underscores the critical importance of such a system, as evidenced by the fact that more than 80 percent of content consumed on Netflix is attributed to their recommendation engine. Therefore, the core issue at hand is the development of a movie recommendation system that not only effectively suggests movies but also maximizes customer satisfaction with Fmovies' streaming service.


## Objectives

**Main Objectives**

Develop a movie recommendation system that provides streaming users with top movie suggestions based on their preferred movie ratings and genres.

**Specific Objectives**

1. Calculate the average ratings of movies.
2. Analyze the distribution of movies by genre.
3. Identify the highest-rated and most popular movies.



## Data
The data utilized in this analysis has been sourced from the MovieLens dataset provided by the GroupLens research lab at the University of Minnesota. This dataset comprises 100,836 ratings and 3,683 tag applications across 9,742 movies, generated by a total of 610 users.

The dataset is organized into four distinct CSV files:

1. **Movies.csv**: Each entry in this file, following the header row, corresponds to an individual movie and contains the following information:
   - `movieId`: a unique identifier for each movie
   - `title`: the name of the movie, followed by its year of release
   - `genres`: categories or genres that the movie may fall into, separated by vertical bars (|).

2. **Links.csv**: This file contains identifiers that can be used to establish links between this dataset and other external sources like IMDb. Each row after the header provides information about one IMDb link, and includes the following columns:
   - `movieId`: a unique identifier for each movie as used by (<a href="https://movielens.org"> Movielens</a>)
   - `imdbId`: a unique identifier for each movie as used by (<a href="http://www.imdb.com"> IMDB</a>)
   - `tmdbId`: a unique identifier for each movie as used by (<a href="https://www.themoviedb.org."> Themoviedb</a>)

3. **Tags.csv**: Each entry in this file, beyond the header row, represents a single tag applied to a particular movie by a specific user. It includes the following information:
   - `userId`: a unique identifier for each user
   - `movieId`: a unique identifier for each movie
   - `tag`: user-generated metadata about the movie in the form of concise, meaningful phrases
   - `timestamp`: the time when the tag was provided by the user.

4. **Ratings.csv**: Each line after the header row in this file represents a single rating and contains the following details:
   - `userId`: a unique identifier for each user
   - `movieId`: a unique identifier for each movie
   - `rating`: the rating given by the user for the movie, using a 5-star scale with increments of 0.5
   - `timestamp`: the time when the rating was given.
   
   **User IDs**: Have been anonymized and randomly selected for inclusion. These IDs are consistent between ratings.csv and tags.csv, meaning the same ID corresponds to the same user in both files.

**Movie IDs**: are assigned only to movies with at least one rating or tag. They align with the IDs used on the MovieLens website (e.g., id 1 corresponds to the URL (<a href="https://movielens.org/movies/1)"> Here</a>). Movie IDs are consistent across ratings.csv, tags.csv, movies.csv, and links.csv.

## Model
**Model Performance**:

Among the collaborative filtering (CF) models evaluated, SVD emerged as the best-performing model based on RMSE. This indicates that SVD provided the most accurate predictions for user ratings.
Hybrid Recommender:

The hybrid recommendation system effectively combines collaborative filtering (CF) and content-based filtering (CB) techniques to provide movie suggestions. This approach leverages both user preferences and movie features for more personalized recommendations.


# Model Evaluation
We assessed our movie recommendation system by examining the derived top 5 movie recommendations for real users in our samples and a new user (an author). In general, our recommendations for existing customers seemed not far from their preferences. 

## Conclusion

The project successfully developed a hybrid recommendation system that combines collaborative filtering (CF) and content-based filtering (CB) techniques. Through extensive evaluation, it was determined that the Singular Value Decomposition (SVD) CF model outperformed other CF models based on RMSE.

The hybrid system incorporates both user preferences and movie attributes, resulting in diverse recommendations spanning genres like Adventure, Drama, Comedy, and Romance. While the recommendations exhibit high accuracy, there is room for further customization to align more closely with individual user tastes.

## Recommendation

1. `Enhanced Personalization`:
Integrate user-specific data like viewing history and preferences for fine-tuning recommendations.

2. `Advanced Collaborative Filtering`:
Explore advanced CF techniques (e.g., FunkSVD, NMF) to potentially boost recommendation accuracy.

3. `Feature Enrichment`:
Augment content-based filtering by incorporating additional movie attributes like actors and directors.

4. `Continuous Evaluation`:
Regularly assess system performance using appropriate metrics to ensure high-quality recommendations.

5. `User Feedback Loop`:
Implement a feedback loop to collect user opinions and refine the system accordingly.

6. `A/B Testing`:
Conduct A/B testing to validate the effectiveness of any implemented changes.
By implementing these suggestions and maintaining a feedback-driven approach, the recommendation system can evolve to deliver increasingly personalized and relevant movie suggestions for users.