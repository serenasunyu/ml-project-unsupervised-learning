# machine_learning_project-unsupervised-learning

### Dataset
Wholesale Data

### Project Goals
1. Data cleaning, data visualization - explore and get inforamtion from the dataset.
2. Preprocess the data
3. Perform KMeans clustering and hierarchical clustering
4. Perform PCA

### Approaches
1. Check duplicates, null values, data typys, outliers and plot heatmap for correlation between variables, box plot for detecting outliers and histograms for distribution of each feature.
2. Using one-hot encoding to handle categorical features and log-transform to handle outliers.
3. Using KMeans clustering and hierarchical clustering to group similar products together and plot elbow method to determine the optimal number of clusters. Using silhouette_score to measure of cluster quality.
4. Using PCA to reduce dimension. The original dataset has too many dimensions which is really hard to view and analyze.

### Result
1. No missing values. 
2. No duplicates.
3. Channels and Regions are categorical variables.
4. The means and standard deviations for each feature vary significantly. It means the range of values for each feature has a huge difference. Need to do feature scaling.
5. There are outliers for some of the features.
6. The elbow method can determine the optimal value of the number of clusters k. Selecting too many clusters may lead to WCSS(Within-Cluster Sums of Squares) of 0 while too few may result in high WCSS. From the elbow plot, we can the the optimal number of cluster maybe 4, 5 or 6. To determine which number is the appropriate bumber cluster, we can use Silhouette Score to valuate the cluster quality. we can see 4 has a higher values and staring from 4, the scores decreased. So 4 cluster is the ideal number in this case. Compared with the Hierarchical Clustering Dendrogram, elbow plot is more straitforward.
7. From Hierarchical Clustering Dendrogram, we can see how clusters are merging at different distances. From my understanding, the level of 4 is an approporiate distance. 
7. We can visualize the clusters via pairs of variables. In order to do that efficiently and make it iterprets the model better, we have to reduce the dimensionality. By using PCA, we find out the optimal number of components is 7. It can explain 96% of the total variance. From the visualization, it is still difficult to grap the clusters when there are 7 components. However, when reducing the number to 2, we barely get any information. It seems like choosing 7 components could provide better results.

### Challenges:
1. After preforming PCA, we reduce the dimension to 7, however, the individual features that contributed to each principal component are not explicitly provided by PCA itself. We still do not know which original features contribute most to each principal component. Further work need to be done.

