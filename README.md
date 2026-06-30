# K-means Clustering

## Assignment Information

- **Student Name:** Mpayimana Cyiza Landry
- **Assignment Title:** K-means Clustering
- **Course:** Unsupervised Machine Learning
- **Schooll:** Stanford University

---

## Assignment Overview

In this practice lab, I implemented the K-means clustering algorithm from scratch and applied it to image compression. The assignment involved understanding unsupervised learning concepts and using clustering to reduce the number of colors in an image while preserving its visual quality.

---

## What I Learned

### 1. **K-means Algorithm Fundamentals**
- Understood the concept of unsupervised learning and clustering
- Learned how K-means groups similar data points together into clusters
- Understood the iterative nature of the algorithm (cluster assignment and centroid update)

### 2. **Cluster Assignment Phase**
- Implemented finding the closest centroid for each data point
- Used Euclidean distance (L2-norm) to measure similarity
- Created an indexing system to track which cluster each point belongs to

### 3. **Centroid Update Phase**
- Implemented recomputing centroids as the mean of assigned points
- Learned that centroids move toward the center of their assigned clusters
- Understood that the algorithm converges to a local optimum

### 4. **Random Initialization**
- Learned the importance of random centroid initialization
- Understood that different initializations can lead to different clustering results
- Implemented random selection of initial centroids from the dataset

### 5. **Image Compression Application**
- Applied K-means to reduce the number of colors in an image from thousands to 16
- Learned about RGB color representation (24-bit color)
- Understood how to reshape image data for clustering
- Calculated compression ratios and storage savings

---

## What I Accomplished

### ✅ Implemented Core Functions

1. **`find_closest_centroids(X, centroids)`**
   - Computed the closest centroid for each training example
   - Used Euclidean distance to measure similarity
   - Returned an array of centroid indices for all data points

2. **`compute_centroids(X, idx, K)`**
   - Computed new centroids by taking the mean of assigned points
   - Handled the case of empty clusters gracefully
   - Returned updated centroid positions

### ✅ Visualized Algorithm Progress

- Observed the step-by-step movement of centroids during iterations
- Visualized how data points are assigned to different clusters
- Understood the convergence behavior of the algorithm

### ✅ Applied K-means to Real Data

- **Toy Dataset**: Successfully clustered a 2D dataset to understand the algorithm mechanics
- **Image Compression**: Applied K-means to compress a bird image
  - Reduced color palette from thousands of colors to 16
  - Achieved approximately 6x compression (393,216 bits → 65,920 bits)
  - Maintained visual quality while significantly reducing storage requirements

---

## Technical Implementation

### Technologies Used
- **Python 3**
- **NumPy** - for numerical computations
- **Matplotlib** - for visualizations
- **Jupyter Notebook** - for interactive development

### Key Functions Implemented

```python
def find_closest_centroids(X, centroids):
    # Assign each data point to the closest centroid
    
def compute_centroids(X, idx, K):
    # Compute new centroids based on assignments
    
def kMeans_init_centroids(X, K):
    # Randomly initialize centroids from data points
    
def run_kMeans(X, initial_centroids, max_iters):
    # Run the complete K-means algorithm