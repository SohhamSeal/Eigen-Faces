# Eigen-Faces
## Overview
Image datasets often have large dimensions, even when resized to a smaller format like (100x100). A resized image of this size results in a flattened image vector with 10,000 values. When dealing with multiple images, these vectors are concatenated column-wise to form a large matrix of size MxN, where M is the size of the flattened image and N is the number of images.

However, the sheer size of this matrix can be computationally expensive and may not capture the essential features of the dataset effectively. To address this, we employ Principal Component Analysis (PCA) to reduce the dimensionality while preserving the variance of the dataset. The outcome of this process is a set of principal components known as "eigenfaces."

## How It Works
### Flattening Images:

Resized images are flattened to create column vectors, resulting in a matrix where each column corresponds to a flattened image.
Concatenation:

These column vectors are concatenated to form a large matrix MxN.
### Principal Component Analysis (PCA):

PCA is applied to this matrix to reduce its dimensionality.
The principal components obtained represent the directions in the dataset where the variance is maximized.
### Eigenfaces:

The principal components, when reshaped, become the eigenfaces.
Each eigenface is a unique direction in the image space that captures important features of the dataset.

## Results
The eigenfaces obtained represent the most significant features in your dataset. These can be used for facial recognition, image compression, or other applications where capturing essential features is crucial.

