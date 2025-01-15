# K-Means Image Compression
![Original and Compressed Image](https://raw.githubusercontent.com/amerob/image-compression-kmeans/main/images/figure%203.png)

## Overview:
This notebook uses the **K-Means clustering algorithm** for **image compression**. It reduces the number of colors in an image by clustering similar colors and replacing each pixel with the centroid of its cluster, preserving visual quality while reducing file size.

### Key Steps:
1. **K-Means Initialization (`kMeans_init_centroids`)**: Randomly selects `K` pixels as centroids.
2. **Assigning Closest Centroids (`find_closest_centroids`)**: Assigns each pixel to the nearest centroid based on Euclidean distance.
3. **Updating Centroids (`compute_centroids`)**: Recalculates centroids by averaging the pixels assigned to each.
4. **Image Compression**: Replaces each pixel with its assigned centroid's color, reducing the image's color complexity.

### Key Functions:
- **`kMeans_init_centroids(X, K)`**: Initializes `K` centroids.
- **`find_closest_centroids(X, centroids)`**: Assigns pixels to the closest centroid.
- **`compute_centroids(X, idx, K)`**: Updates centroids based on pixel means.

### How it Works:
1. **Data Preparation**: Flatten the image into a 2D array of RGB values.
2. **Cluster Assignment**: Assign each pixel to the closest centroid.
3. **Centroid Update**: Recalculate centroids by averaging assigned pixels.
4. **Compression**: Reconstruct the image by replacing each pixel with its centroid color.

### Usage:
- **Input Image**: Load and flatten an image into a 2D array.
- **Compression**: Reconstruct the image with fewer colors after applying K-Means.

This notebook demonstrates how **K-Means** can reduce image size while maintaining visual quality, useful for **image storage** and **network transmission**.
