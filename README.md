# RecommendationEngine
Online Movie Recommendation Engine using K-Nearest Neighbors Machine Learning Algorithm
KNN is a simple concept: define some distance metric between the items in your dataset,
and find the K closest items. You can then use those items to predict some property of a
test item, by having them somehow "vote" on it.

The test sample (green circle) should be classified either to the first class of blue squares or to the second
class of red triangles. If k = 3 (solid line circle) it is assigned to the second class because there are 2 triangles
and only 1 square inside the inner circle. If k = 5 (dashed line circle) it is assigned to the first class (3 squares
vs. 2 triangles inside the outer circle).
The special case where the class is predicted to be the class of the closest training sample (i.e. when k = 1) is
called the nearest neighbor algorithm.
Choice of k is very critical – A small value of k means that noise will have a higher influence on the result. A
large value make it computationally expensive and kinda defeats the basic philosophy behind KNN (that
points that are near might have similar densities or classes)
A simple approach to select k is set k = n^(1/2). Usually, the rule of thumb is squareroot of number (n) of
features.
Source : Wikipedia and dtio research

In this example, we will use Cosine Distance.
Math Refresher: Calculating Cosine Distance. How to compute Cosine distance and
Similarity?
spatial.distance.cosine computes the distance, and not the similarity. You subtract the
value from 1 to get the similarity.

We will use MovieLens data. We will get 10 nearest neighbors for a given movie


