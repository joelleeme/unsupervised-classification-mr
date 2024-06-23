# Mushroom Classification: Safe to Eat or Deadly Poison?
### Overview
This project aims to classify mushrooms based on their characteristics as either safe to eat or potentially deadly. The dataset contains descriptions of various mushroom features such as cap shape, odor, gill size, and more. Each mushroom species is categorized as definitely edible, definitely poisonous, or of unknown edibility (combined with the poisonous category for simplicity).

### Dataset
The dataset used in this project is sourced from the Audubon Society Field Guide and can be downloaded from Kaggle:
[Mushroom Classification Dataset on Kaggle](https://www.kaggle.com/datasets/uciml/mushroom-classification)

### Project Structure
The repository is structured as follows:
Unsupervised_Algorithms.ipynb: Jupyter notebook for data exploration, preprocessing, and modeling.
README.md: This readme file.

#### Data Preprocessing
The preprocessing steps include:
1. Loading the dataset from mushrooms.csv.
2. Handling missing values in the 'stalk-root' column by replacing '?' with the mode.
3. Encoding categorical variables using LabelEncoder from sklearn.

#### Exploratory Data Analysis (EDA)
Key EDA steps include:
1. Class Distribution: Visualizes the distribution of edible vs. poisonous mushrooms.
2. Cap Shape Distribution by Class: Shows variations in cap shapes between edible and poisonous mushrooms.
3. Correlation Heatmap: Displays the pairwise correlations between numeric features.

#### Unsupervised Learning Models
##### K-Means Clustering
K-Means clustering is used to partition the data into clusters. We explored different values of K to find the optimal clustering configuration.

##### DBSCAN Clustering
DBSCAN, a density-based clustering algorithm, groups closely packed points and marks outliers as noise. We optimized the eps and min_samples parameters for better performance.

##### PCA + K-Means Clustering
PCA was applied to reduce the dimensionality of the data for visualization. K-Means was then applied to the PCA-reduced data to analyze clustering performance.

#### Results and Discussion
K-Means Clustering: Achieved a Silhouette Score of 0.3120 with K=6 clusters.
DBSCAN Clustering: Improved V-measure to 0.2140 with optimized parameters.
PCA + K-Means Clustering: Visualized clustering with a Silhouette Score of 0.1863.
