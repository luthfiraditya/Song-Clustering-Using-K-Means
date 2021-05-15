# Song-Clustering-Using-K-Means
<br>

#### what is K-Means ?
K-Means is an unsupervised learning algorithm (meaning there are no target labels) that allows you to identify similar groups or clusters of data points within your data. The group based on their distance to the centroid (A centroid is just the mean (average) position of all points in a cluster).

**K-Means process** :


**Dataset description** :
SpotifyFeatures.csv
genre:the genre of the track;
artists_name:The list of artists credited for production of the track,
popularity: the popularity rate of the track,
danceability:The relative measurement of the track being danceable,
energy: The energy of a song - the higher the value, the more energtic,
liveness: The higher the value, the more likely the song is a live recording,
valence : The higher the value, the more positive mood for the song,
loudness :  the louder the song,
liveness : The higher the value, the more likely the song is a live recording,
instrumentalness: The relative ratio of the track being instrumental,
tempo : is the speed or pace of a given piece,

## Data Preprocessing

**import library**
-for anlalyzing data we use pandas and numpy library,
-visualizing data we use matplotlib and seaborn,
-for machine learning mostly we use sklearn.


**understanding data**
To begin this step, We use the info() function to get a quick and dirty overview of variable datatypes and describe() to get some basic statistical.

**Data Cleaning**
is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset.
This data is usually not necessary or helpful when it comes to analyzing data because it may hinder the process or provide inaccurate results
<br>
there are 3 problem
1. missing value
2. there are problem in  data, we must delete ";;;" so we can convert it into numeric data type
3. the data type is object so we can't procces it, we must convert it into numeric data type like float or integer

<br>

### Data Transformation
standardization is used because it relates to PCA(Principan Component Analysis)

standardization (or Z-score normalization) is that the features will be rescaled so that they’ll have the properties of a standard normal distribution with
μ=0 and σ=1

**PCA**
<br>
Principal Component Analysis, or PCA, is a dimensionality-reduction method that is often used to reduce the dimensionality of large data sets, by transforming a large set of variables into a smaller one that still contains most of the information in the large set.
<br>
So, the idea is 13-dimensional data gives you 13 principal components, but PCA tries to put maximum possible information in the first component, then maximum remaining information in the second and so on, until having cumsum = 1(total).
evr shows how much variance is explained by each of the fourteen features

K-Means Clustering
to determine the optimal number of clusters let's use elbow method with distortion( It is calculated as the average of the squared distances from the cluster centers of the respective clusters. Typically, the Euclidean distance metric is used.)
<br>
“what exactly is the distortion?”. The distortion is the sum of square errors (SSE)
The “error” in this case is the difference between each data point coordinates and the centroid coordinates.
The SSE is simply:

All we’re doing is:
1. taking the difference between each data point and a centroid
2. squaring that difference
3. and summing it all up!

## Conclusion

1. With PCA we can reduce data from 13 data variables into 8 components and can be used in K-Means modeling
2. With K-Means we can group the songs in the data into 8 clusters, based on the attributes they have such as acousticness, danceability, energy etc.

Moreover, using K-Means algorithm, we can create a song recommendation system based on the attributes that each variable has.


