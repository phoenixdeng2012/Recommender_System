# Recommender_System

## Content based filtering KNN:

Each movie comes with its characteristics that are associated with its content. For example genres. We can make an array out of it. We can define how similar two movies are based on cosine similarity score.

Content based filtering works like this:

First you calculate a similarity matrix for all combinations of movies, for example you have n movies, then the matrix is nxn.
Let's say you want to predict movie I, then you look up for the similarity of movie I to other movies a user has rated, you find k most similar movie and average the rating by the their similarity score.

## Collaborative filtering:

It's recommending stuff based on other people's collaborative behavior. Finding users that like you and recommend stuff that they like but you haven't seen yet.

### 

