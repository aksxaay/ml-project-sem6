### machine learning project

Ripped Links
[Recommender-Systems-Using-RBM](https://github.com/nitwmanish/Recommender-Systems-Using-RBM)
[namthatman // Recommender-System](https://github.com/namthatman/Recommender-System/tree/master/4.%20Deep%20Learning%20for%20Recommender%20Systems)


> CREDIT: Udemy course, "Building Recommender Systems with Machine Learning and AI", by Sundog Education by Frank Kane, Frank Kane

RBM - Res
RBM became popular after Netflix competition as ot was used as a collaborative filtering strategy to forecast user ratings to movies and it outperformed all of its other rivals
RBM is a graphical model for unsupervised learning that is used to discover hidden structures in data.
Video Recommendations are just the perfect recommendation for that.

Visible -> Hidden
Restricted comes from "no node is connected to any other node in the same layer"

Phase
+ve associations
-ve associations
Feed Forward Pass - RBM
Feed Backward Pass - RBM

Ensemble models - combining multiple other models, combine decision from multiple other models.
basically learning prob distribution across our entire dataset. 
- features extraction
- pattern recognition
- structure in datasets
- hierarchy in events

Content Based Filtering - ppt make.

> **Collaborative Filtering** To address some of the limitations of content-based filtering, collaborative filtering uses similarities between users and items simultaneously to provide recommendations.


[collab filter vs content filter](https://analyticsindiamag.com/collaborative-filtering-vs-content-based-filtering-for-recommender-systems/)

Recommendation Engines
- content
- collaborative


## collab

- based on past interactions that have been recorded with users and items, - Amazon?
- Collaborative Filtering tends to find what similar users would like and the recommendations to be provided and in order to classify the users into clusters of similar types and recommend each user according to the preference of its cluster.

- past user-item interaction

The standard method used by Collaborative Filtering is known as the Nearest Neighborhood algorithm.


Challenges with Collaborative Filtering
The only issue with this method is that the prediction of the model for a given user, 

item pair is the dot product of the corresponding embeddings. 

So, if an item is not seen during training, the system cannot generally create an embedding for it and hence cannot query the model with this item. This issue is known as the **cold-start problem**.


### content
uses additional information about users / items

item features to recommend other items similar to what the user likes and also based on their previous actions or explicit feedback.

Movie Recommendation System
Additional information can be
- age
- sex
- job
- personal information
- category
- main actors
- duration
- items
- etc

main concept - try and build a model based on available **features**

Utility Matrix - signifies user's preference for certain items.
relation of those liked vs disliked

value is assigned to each user-item pair
known as *degree of preference*

matrix of user is drawn with the items to identify their preference relationship.

Challenges.
no cold-start problem.
only new users or items with unseen features will logically suffer from this drawback.

similar items are grouped based on their features.

user profiles are constructed

item based filtering.

pivot table function


### Collaborative Filtering Vs Content-Based Filtering
Here is a list of points that differentiate Collaborative Filtering and Content-Based Filtering from each other :

The Content-based approach requires a good amount of information about items’ features, rather than using the user’s interactions and feedback. They can be movie attributes such as genre, year, director, actor etc. or textual content of articles that can be extracted by applying Natural Language Processing. Collaborative Filtering, on the other hand, doesn’t need anything else except the user’s historical preference on a set of items to recommend from, and because it is based on historical data, the core assumption made is that the users who have agreed in the past will also tend to agree in the future.  
Domain knowledge in the case of Collaborative Filtering is not necessary because the embeddings are automatically learned, but in the case of a Content-based approach, since the feature representation of the items is hand-engineered to an extent, this technique requires a lot of domain knowledge to be fed with.  
The collaborative filtering model can help users discover new interests and although the ML system might not know the user’s interest in a given item, the model might still recommend it because similar users are interested in that item. On the other hand, A Content-based model can only make recommendations based on the existing interests of the user and the model hence only has limited ability to expand on the users’ existing interests. 
A Content-Based filtering model does not need any data about other users, since the recommendations are specific to a particular user. This makes it easier to scale down the same to a large number of users. A similar cannot be said or done for Collaborative Filtering Methods. 
The collaborative algorithm uses only user behavior for recommending items while for Content-based filtering we have to know the content of both user and item.


### Conclusion
- collab - users user behavior
- content - both user and item.

k means - clustering
k nearest neighbour - classification algorithm.

dataset of basketball players positions, measurements
- want to assign positions to basketball players, in a new dataset where measurements but no positions
- k nearest neighbours

however if dataset of basketball players who need to be grouped into k distinct groups based off of similarity
- k means


RBM - pattern recognition? Deep Learning?
shallow 2 layer net

visible connected to hidden

[RBM ep6 deep learning.](https://www.youtube.com/watch?v=puux7KZQfsE)
math equivalent of a 2 way translater
- forward pass
- backward pass

KL divergence (relative entropy information gain)

interesting aspect of RBM is that a data does not need to be labelled
- photo
- videos
- voices
- sensor data
- can't label data
- auto sorts data

chooses which input features 
RBM -> feature extractor neural net (auto encoders)
- they have to encode their own structure.


[tensorflow content & collab filtering](https://www.youtube.com/watch?v=v90un9ALRzw)


content-based filtering
- recommending items based on attributes of those items themselves instead of trying to aggregate user behavior data.

eg, same actors, same directors

Content Based Similarity: 
- Cosine similarity, 
- Multi-dimensional Cosine, 
- Time Similarity

K - Nearest Neighbours.
- content based similarity scores between this movie and all others the user rated
- select/sort some number
- k of the nearest-neighbours to the movie
- top k nearest
- take the weighted average of similarity scores weighting by the rating the user gave
- rating prediction.


### Challenges of Recommender Systems
- cold start problem
- stoplists
- filter bubbles trust
- outliers
- gaming the system


[developers.google](https://developers.google.com/machine-learning/recommendation/overview/candidate-generation)

Candidate Generation Overview

Candidate Generation is first stage of recommendation

- content -> user A watches 2 cute cat videos, the system recommends a cute animal video
- collaborative -> if user A is similar to user B who likes Video 1, then the system can recommend video 1 to user A as well.


Why are we using KNN
- item-based collaborative filtering, KNN is perfect go-to model and also a very good baseline for recommender system development.
- KNN does not make any assumptions on the underlying data distribution but it relies on item feature similarity.