# GNR602-Course-Project
Model to Detect Changes in Multi-Temporal Satellite Images Using PCA and K-means Clustering Techniques

``` bash
Directory
├── README.md
├── LICENSE
├── requirements.txt
├── setup.py
├── build
│   └──exe.win-amd64-3.9
│      ├── frozen_application_license.txt
│      ├── python3.dll
│      ├── python39.dll
│      ├── simple.exe
│      └── lib
├── Input Image
│   ├── Andasol_09051987_md.jpg
│   └── Andasol_09122013_md.jpg
└── Output Image
    └── changed.jpg
```

# Principal Component Analysis (PCA) for Multi-Temporal Satellite Image Change Detection

The application uses PCA and K-Mean algorithm to detect the change between multi-temporal Satellite image. The application takes two images as input and display and save the output image.

## Introduction

Principal Component Analysis (PCA) is a technique used to reduce the dimensionality of a dataset. It can be used to identify patterns in data, and is often used in image processing applications.

K-Mean is a widely used clustering algorithm which divides the data into required region by calculating the centroids which best fit to the respective regions. 

Multi-Temporal Satellite Image Change Detection is the process of analyzing satellite imagery taken at different times to identify changes that have occurred in the landscape. This can be useful in a variety of applications, such as tracking the progression of urbanization or monitoring the effects of natural disasters.

PCA can be used in Multi-Temporal Satellite Image Change Detection to identify the principal components that contribute to the observed changes between the images. The K-Mean algorithm is used to divide the changed part and 
unchanged part between the two image.
## Requirements

The following libraries are required to implement PCA for Multi-Temporal Satellite Image Change Detection:

- NumPy
- Collections
- OpenCV
- Tkinter
- customtkinter
- PIL
- MatplotLib

## Implementation

1. Two satellite images were taken as input. The images were resized and the absolute difference of the images were taken.

2. The difference image was passed through a function which converts the image array into 5x5 non overlapping blocks and returns the vector set and mean of each feature of the vector set.

3. The vector set was passed through the PCA function which returns the sorted eigen vector matrix in descending order of eigen values.

4. The Eigen Vector Set(EVS) is then passed through a function which returns the projection of EVS on 5x5 overlapping blocks of the difference image i.e Feture vector set (FVS). 

5. The feature vector set is passed through the K-Mean clustering function which returns the image with cluster as the changed part and unchanged part.

6. The changed part is assigned the bright(255) pixel and the unchanged part is assigned the dark values(0).





