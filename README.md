# Milkfish-Fry-Counter


## Introduction
The approach of this Fish Fry counter focuses on the image segmentation through the use of thresholding. It applies the OTSU Method to simplify the values automatically without the tedious process of manually fine-tuning the parameters.

Here's the summary of the accuracy results based on the average contour detection as well as standard deviation

| Actual | Avg Fry Count | Accuracy |   SD   |
| :----: | :-----------: | :------: | :----: |
| 100    | 97.765        | 97.77%   | 3.272  |
| 200    | 182.618       | 91.31%   | 8.484  |
| 300    | 294.78        | 98.26%   | 21.051 |
| 400    | 349.42        | 87.36%   | 29.363 |

## Fry Counter Approach

Grayscale --> Crop --> Filtering: Gaussian filtering --> Image Segmentation: OTSU Threshholding --> Contours --> Detection