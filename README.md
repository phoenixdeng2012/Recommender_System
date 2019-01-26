# Recommender_System

## Content based filtering KNN:

Each movie comes with its characteristics that are associated with its content. For example genres. We can make an array out of it. We can define how similar two movies are based on cosine similarity score.

Content based filtering works like this:

First you calculate a similarity matrix for all combinations of movies, for example you have n movies, then the matrix is nxn.
Let's say you want to predict movie I, then you look up for the similarity of movie I to other movies a user has rated, you find k most similar movie and average the rating by the their similarity score.

## Collaborative filtering:

It's recommending stuff based on other people's collaborative behavior. Finding users that like you and recommend stuff that they like but you haven't seen yet.

At the heart of recommender system are ways to measure similarity. Similarity to measure users or items or contents.

### User based collaborative filtering:

Find other users similar to yourself and recommend stuff they liked but you haven't seen it yet.

  - from user->item rating matrix, we can calculate user->user similarity matrix
  - Look up K nearest candidates that are similiar to a user (Bob for example) we want to recommend to
  - line up all movies users watched in last step and give them a score based on user rating and user similarity with Bob.     Last we need filter out movies that Bob already watched, and set a minimum score threshold.
  - [User Based Collaborative Filtering Code](https://github.com/phoenixdeng2012/Recommender_System/blob/master/User_based_collaborative_filtering.ipynb)

### Item based collaborative filtering:

Recommend items that are similiar to what a used purchased before.

  - from item->user matrix, we can calculate item->item similarity matrix.
  - find 10 most liked items by a user (Bob)
  - find top 40 most similiar items to the top 10 items a user liked
  - [Item based Collaborative Filtering Code](https://github.com/phoenixdeng2012/Recommender_System/blob/master/Item_based_collaborative_filtering.ipynb)
  
 ### Matrix Factorization:
 
 The user rating matrix can be factorized as a product of user matrix (rows are users, columns are latent features) and item matrix.
 
 - [Matrix Factorization Code](https://github.com/phoenixdeng2012/Recommender_System/blob/master/Recommending_System_SVD.ipynb)
 
### AutoEncoder:

Typically deep learning based recommender system faces challenge of how to deal with sparse matrix in matrix multiplication. There is no easy way to ignore items where there is no rating in matrix multiplication. Some method just deal with no rating as 0s and ignore them, this basically treat missing values as if the users hate those movies since the rating is 0. The code just simply treat missing value as 0.

- [AutoEncoder](https://github.com/phoenixdeng2012/Recommender_System/blob/master/AutoEncoder%20Recommender%20System.ipynb)
  

