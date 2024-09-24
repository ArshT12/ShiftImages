Image Analysis and SIFT Keypoint Extraction Project
Project Overview
This project utilizes OpenCV and SIFT (Scale-Invariant Feature Transform) to extract keypoints and descriptors from one or more images. It also includes functionality to perform k-means clustering on the SIFT descriptors and compute a dissimilarity matrix to compare multiple images based on their feature clusters. This project is particularly useful for tasks involving image matching, feature detection, and clustering.

Key Features
1. Rescale Images
The images are rescaled to a target size of 480x600 pixels while maintaining their aspect ratio. This ensures that images are uniformly processed without distorting their content, which is crucial for consistent feature extraction.
2. SIFT Keypoint Detection (Task 1)
SIFT is used to detect keypoints and compute descriptors from images. It is a powerful method for extracting invariant features that can be used for tasks like object recognition or image matching.
The SIFT keypoints are visualized and displayed alongside the original image.
3. SIFT Feature Extraction for Multiple Images (Task 2)
For multiple images, SIFT is used to extract keypoints and descriptors from each image, which are then used for clustering and comparison.
Keypoints are detected across multiple images, and the descriptors are saved for further analysis.
4. K-Means Clustering on SIFT Descriptors
After extracting SIFT descriptors, k-means clustering is applied to group similar features together.
Clustering is performed for three different configurations:
5% of total keypoints
10% of total keypoints
20% of total keypoints
K-means helps in segmenting the images into clusters based on the extracted SIFT descriptors, providing a foundation for image comparison.
5. Building Normalized Histograms
Histograms are created for each image, representing the frequency of cluster assignments for each feature. These histograms are normalized so that they can be effectively compared between images.
6. Dissimilarity Matrix Calculation
The Chi-square distance metric is used to compute a dissimilarity matrix between the histogram representations of images. This matrix provides a quantitative comparison of how similar or different two images are based on their SIFT features.
7. Dissimilarity Matrix Visualization
The dissimilarity matrix is printed to the console, showing the relative distance between all image pairs for each clustering configuration (5%, 10%, 20%). This allows easy comparison of the feature-based similarity between multiple images.
Project Structure
A2maybe.py: The main Python script that contains all the functions for image processing, feature extraction, and clustering.
requirements.txt: The dependencies required to run the project.
images/: The folder where you can store sample images to be processed.
