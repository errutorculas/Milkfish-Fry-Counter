# Milkfish-Fry-Counter


## Introduction
The approach of this Fish Fry counter focuses on the image segmentation through the use of thresholding. It applies the OTSU Method to simplify the values automatically without the tedious process of manually fine-tuning the parameters.

---
### Contour Detection

Here's the summary of the accuracy results based on the average contour detection as well as standard deviation

| Actual | Avg Fry Count | Accuracy |   SD   |
| :----: | :-----------: | :------: | :----: |
| 100    | 97.765        | 97.77%   | 3.272  |
| 200    | 182.618       | 91.31%   | 8.484  |
| 300    | 294.78        | 98.26%   | 21.051 |
| 400    | 349.42        | 87.36%   | 29.363 |
---
### Feature Detection
Feature detection is designed to identify specific points or patterns in an image that are relevant to a particular task, such as object recognition or tracking. Features can include points, corners, edges, or other distinctive visual patterns that can be used to identify or match objects across multiple images. Feature detection is often more robust than contour detection, as it can be designed to be invariant to changes in lighting, scale, and orientation. However, feature detection algorithms can be more complex and computationally intensive than contour detection algorithms.

For object tracking/detection, Oriented FAST and Rotated BRIEF (ORB) is used to look at the features of the segmented image.

Here's the summary of the accuracy results based on the average feature detection as well as standard deviation

| Actual | Avg Fry Count | Accuracy |   SD   |
| :----: | :-----------: | :------: | :----: |
| 100    | 98.314        | 98.31%   | 5.293  |
| 200    | 194.618       | 97.31%   | 4.712  |
| 300    | 294           | 98%      | 10.244 |
| 400    | 389.34        | 97.34%   | 18.272 |

---
## Fry Counter Approach

Grayscale --> Crop --> Filtering: Gaussian filtering --> Image Segmentation: OTSU Threshholding --> Detection