# K-Means-Clustering
## Image Compression Using K-Means Clustering

This repository contains code to perform image compression using the K-Means clustering algorithm. The implementation involves functions for finding the closest centroids, computing new centroids, and running the K-Means algorithm iteratively. The code is applied to compress an image by reducing the number of unique colors while maintaining visual similarity.

## Table of Contents
- [Introduction](#introduction)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Functions](#functions)
  - [find_closest_centroids](#find_closest_centroids)
  - [compute_centroids](#compute_centroids)
  - [run_kMeans](#run_kmeans)
  - [kMeans_init_centroids](#kmeans_init_centroids)
- [Image Compression Example](#image-compression-example)
- [Results](#results)

## Introduction
The K-Means clustering algorithm is used to compress images by reducing the number of unique colors. This is achieved by clustering the pixels in the image into a predefined number of clusters and replacing each pixel's color with the nearest cluster centroid.

## Dependencies
- numpy
- matplotlib
- utils (custom utility functions, ensure this is in your path)
- public_tests (custom utility functions, ensure this is in your path)

## Usage
1. Clone the repository.
2. Ensure the dependencies are installed.
3. Run the code cells in the provided Jupyter notebook or script.

## Functions

### find_closest_centroids
This function computes the closest centroid for each data point in the dataset based on the initial centroids.

### compute_centroids
This function calculates new centroids by averaging the data points assigned to each centroid.

### run_kMeans
This function executes the K-Means algorithm iteratively, updating the centroids and assigning data points to the closest centroids.

   ***K-means iteration = 9***

![k-means-iteration9](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/8ef62e53-c8ab-44d8-b7b8-d8baa7e56e11)


### kMeans_init_centroids
This function initializes centroids by randomly selecting K data points from the dataset.

  ***K-Means iteration = 9, when K=3***
![k-Means-iteration-9-when-k=3](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/b677a608-e0ad-4109-91f2-391569614672)
## Image Compression Example
The provided code compresses an image of a bird by reducing the number of unique colors using the K-Means algorithm.

### Steps
1. **Load and Display the Image**:
   Load the image and display its shape.
![Image compression with K-means](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/ffd600c9-48ee-4684-95d5-047a0922b99c)

3. **Preprocess the Image**:
   Reshape the image into a 2D array where each row represents a pixel's RGB values.

4. **Run K-Means**:
   Run the K-Means algorithm on the image data with 16 clusters and 10 iterations.

5. **Compress the Image**:
   Replace each pixel with the color of the nearest centroid, and reshape the image back to its original dimensions.
 
   ***Plot the colors of the image and mark the centroids***
![kMeans-Plot](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/93345b3c-a292-41b3-9f34-bfbb31f8a3fb)

   ***Centroid colors***
![centroid color](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/c9f08f6f-8651-4429-a907-c14d15425b05)


7. **Display the Original and Compressed Images**:
   Display the original and compressed images side by side.

![compressed image](https://github.com/UMMY87/K-Means-Clustering/assets/117314436/aea2455f-f6fb-4f32-8fa3-539e86e34ee3)
## Results
The original image is compressed by reducing the number of unique colors to 16. The compressed image maintains visual similarity to the original while achieving a significant reduction in color diversity. This demonstrates the effectiveness of K-Means clustering for image compression.
