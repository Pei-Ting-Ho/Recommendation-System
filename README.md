# Recommendation-System

## Interaction Distribution
Given the nature of recommendation problem:
- Most of the users give feedback to only a few items.
- Most of the items receive feedback from only a few users.

<img width="733" alt="Screen Shot 2023-01-29 at 14 35 29" src="https://user-images.githubusercontent.com/62037588/215311787-67885c9c-f841-4e6a-9b2d-2eae309f4885.png">

Then, we are dealt with a sparse user-item interaction matrix:

<img width="1032" alt="Screen Shot 2023-01-29 at 15 06 21" src="https://user-images.githubusercontent.com/62037588/215311903-4b518399-c735-4146-94dd-7ff133a730f7.png">

Thus, we are looking at the matrix completion problem, where if the matrix was fully populated with predicted ratings, we would be able to provide recommendations to a user based on past interaction history.  

## Solution Framework
Here are some common approaches, from non-personalized to personalized recommender models:  
- Rank Based Recommendation System:

  This is a simple and intuitive model, in which we consider:
  - Item Popularity: How many people have interacted with the item?
  - User Preference: How much people have liked or disliked the item?
  
  Based on minimum interactions and average ratings, we could easily provide recommendations to a new user who enters the system and has no records.
- Collaborative Filtering Recommendation System:

  This is a more nuanced model, in which we consider groups of people or items:  
  - User-User KNN Model: In calculating the user similarity, we could provide recommendations to a user based on its neighbors' item preferences. 
  - Item-Item KNN Model: In calculating the item similarity, we could provide recommendations to a user based on its neighbors' item characteristics.
- Matrix Factorization Recommendation System:

  This is a more sophisticated model, in which we perform the matrix decomposition technique (SVD) - User Matrix * Diagonal Matrix * Item Matrix. In doing so, we uncover the latent features describing the underlying patterns and, derive the close approximations to the original matrix. 

