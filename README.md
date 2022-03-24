# Recommender-Systems
## ECE 219 - Project 3

The aim of this project is to build a recommender system. A recommender system is used to predict the rating or preference of a given user. For example, recommender systems are widely used to generate playlists on spotify, to recommend movies on netflix, or to recommend potential products to buy on amazon.

There are two ways to implement these recommender systems: 
- Collaborative Filtering
- Content-based Filtering
Or, we also use a combination of both of the above filtering techniques.

In this project, we will be exploring Collaborative Filtering methods to build a recommender system for a Synthetic Movie Lens Dataset. This dataset contains 100836 ratings and 3683 tag applications across 9742 movies. The underlying rating matrix in this dataset is a sparse matrix which is a main challenge for designing collaborative filtering models. Collaborative filtering is a method that filters the preference of a given user by collecting preferences or ratings from several other users.

The two major types of Collaborative Filtering methods are:
- Neighbourhood-based Collaborative Filtering : We further classify this method into item-based models and user-based models. In this project, we implement the user-based method. To determine the neighbourhood of a given user, we need to first find the similarity between the ratings of the users, which is done by constructing a similarity function using Pearson-correlation Coefficient. We then implement KNN method to define the neighborhood of the users.
- Model-based Collaborative Filtering : In this approach, we deploy ML algorithms to predict the ratings of users for unrated items. In this project, we implement latent factor based models. Here, we implement NMF filter, MF with bias filter, and Naive filter.

To evaluate the performance of these filter models, we use a 10 fold cross validation. We then report the RMSE and MAE values across all these 10 folds and reprt the minimum average RMSE. ROC curves are also plotted to visualize the performance of the various models.
