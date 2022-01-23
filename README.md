# Kaggle-Music-Genre-Clustering

The dataset is about the music genre. The goal is to use the information about the song to predict which genre it belongs to. In this particular project, the goal is to use these features to perform unsupervised classification and use the target to determine the effectiveness of classification.

## EDA
- There are some invalid samples. For example, ‘duration_ms’ = -1.
- In the original dataset, there are 10 genres. To simplify the problem and make the visualization more obvious, we selected 4 genres that are most different from each other. The 4 genres are ‘Anime’, ‘Classical’, ‘Hip-Hop’, and ‘Jazz’.
- One-hot encoding for categorical features and standardize all features.

## K-means
The true cluster is 4. In K-means, we tried number of clusters from 2 to 9. It gives the following adjusted index score (precision of clustering problem).

![image](https://user-images.githubusercontent.com/76148884/150659585-0d46a527-f78b-4d71-8463-7616ca0d5b2f.png)

We can see that when K=4, the adjusted rand index is the highest, which means most consistent with the true classification result.

## Gaussian Mixture Model
GMM is a probabilistic algorithm that uses soft clustering approach for distributing the points in different clusters. The advantages of GMM are that 1) it can analyze more complex and mixed data. 2) It can handle outliers better. 

## PCA
We also applied PCA with n_components=2 to transform the data into two dimensions to visualize it better.

![image](https://user-images.githubusercontent.com/76148884/150659620-7a534fe7-a344-4e20-b514-dd057ff94bb9.png)

The clustering results from both methods are similar to the true clusters, which means the algorithms did good job.

![kmeans](https://user-images.githubusercontent.com/76148884/150659672-2b2364aa-9572-4ee0-89b3-f820f84f71de.gif)

Here is a gif showing the process of clustering as training iterates. 
