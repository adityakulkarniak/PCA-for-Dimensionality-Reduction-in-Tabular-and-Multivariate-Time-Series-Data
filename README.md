# PCA-for-Dimensionality-Reduction-in-Tabular-and-Multivariate-Time-Series-Data
A hands-on project demonstrating Principal Component Analysis PCA for dimensionality reduction on both tabular and multivariate time series data. Covers data generation, scaling, eigen decomposition, variance analysis, and visualization to reveal key patterns and correlations efficiently.

**Objective**
To understand PCA mathematically and geometrically on 3D synthetic data and visualize how eigenvectors represent directions of maximum variance.

**Steps**

Data Generation
Two synthetic classes are created from multivariate normal distributions with different means.
Each observation contains three correlated features and one class label.

**Visualization**

3D scatter plot shows two class clusters in feature space.

**Standardization**
Features are standardized using StandardScaler to make them mean 0 and unit variance.
Standardization ensures that PCA is not biased toward features with larger numerical ranges.

**Covariance Matrix**
Covariance matrix captures relationships between features.
High covariance indicates redundancy between features.

**Eigen Decomposition**

Eigenvalues represent the amount of variance captured by each principal direction.
Eigenvectors represent the directions (axes) of maximum variance.
Visualization of Eigenvectors
Eigenvectors are plotted as red arrows showing the principal axes in feature space.

**Dimensionality Reduction**

Data is projected onto the first two principal components using matrix multiplication.
The new 2D dataset (PC1, PC2) retains most of the original variance while reducing complexity.

**2. PCA for Dimensionality Reduction in Multivariate Time Series Data**

To demonstrate how PCA can compress multiple correlated time-dependent signals into fewer uncorrelated components while preserving underlying trends.

**Steps**

Synthetic Time Series Generation
Four time series (sensors) are simulated.Three are correlated through a common latent signal, and one is independent noise.
This setup represents typical multivariate sensor data in IoT or industrial systems.

**Visualization of Raw Data**

Each sensor signal is plotted to show correlation and redundancy.
Correlated signals exhibit similar trends due to shared underlying patterns.
Standardization
All variables are standardized to equalize scales and prepare for PCA.

**Applying PCA**

PCA is fitted to standardized data using sklearn.decomposition.PCA.
Principal Components (PCs) are computed, and their explained variance ratios indicate how much information each PC retains.

**Explained Variance Analysis**

The first few PCs capture most of the variance, showing effective compression.
Cumulative variance helps decide the optimal number of components.

**Visualization of Reduced Components**
Original correlated sensors and the first principal component (PC1) are plotted together.
PC1 captures the shared pattern across sensors, effectively summarizing the system’s overall behavior.
