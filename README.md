# Clustering with K-Means and Centers Modified to Medoids

This project implements **clustering** using `KMeans` from `scikit-learn` and manually converts the generated cluster centers to **medoids** (i.e., actual data points instead of averages). This technique provides a faster alternative to algorithms like **K-Medoids** or **CLARA** by leveraging the efficiency of K-Means while still using real data points as cluster centers.

## Project Description

The method:
1. Trains a K-Means model.
2. Finds the nearest data point to each cluster center and uses it as the new center (medoid).
3. Updates the K-Means model to use these medoids as cluster centers.

A complete example of use is shared in the notebook

### Why Use This Approach?

The main advantage of this method compared to K-Medoids or CLARA is **speed**. While K-Medoids and CLARA focus on using actual data points as cluster centers, they can be computationally intensive, especially with large datasets. By first running K-Means and then adjusting its centers to the nearest points (medoids), this approach achieves similar results with significantly improved performance.

## Requirements

Install the required libraries:

```bash
pip install numpy matplotlib scikit-learn