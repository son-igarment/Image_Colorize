# Models Directory

**Author: Phạm Lê Ngọc Sơn**

This directory contains the model files required for the Image Colorization project:

1. `colorization_deploy_v2.prototxt` - Model architecture definition file (included)
2. `colorization_release_v2.caffemodel` - Pre-trained model weights (needs to be downloaded)

## Downloading the Model

The `colorization_release_v2.caffemodel` file needs to be downloaded separately due to its large size.
You can download it from the official repository or use a direct download link from reliable sources.

Place the downloaded file in this directory to properly run the colorization tools.

## Model Information

These models are based on the research work for deep colorization. The system uses a CNN (Convolutional Neural Network) approach to predict the ab color channels from the L channel in the Lab color space.
