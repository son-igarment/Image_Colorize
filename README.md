# Image Colorization Tool

**Author: Phạm Lê Ngọc Sơn**

## Overview
This project focuses on transforming grayscale images into vibrant, colored versions using advanced AI and machine learning techniques. The goal is to restore old photographs, add life to monochromatic images, or create artistic renditions of classic visuals.

## Project Structure
- `GUI.py` - Graphical user interface for the colorization tool
- `image_colarization.py` - Core image colorization script
- `Colorize_Black_and_White_Image.ipynb` - Jupyter notebook with colorization process
- `models/` - Directory containing pre-trained models
  - `colorization_deploy_v2.prototxt` - Model architecture definition
  - `colorization_release_v2.caffemodel` (needs to be downloaded) - Pre-trained weights
- `pts_in_hull.npy` - Color points reference for the colorization process
- Various image files (input and output examples)

## How It Works
The colorization tool uses a deep learning model based on a pre-trained Caffe model. The process involves:
1. Converting the input image to LAB color space
2. Extracting the L channel (lightness/luminance)
3. Predicting the ab channels (color information) using the neural network
4. Combining the original L channel with the predicted ab channels
5. Converting back to RGB color space to produce the colorized image

## Requirements
- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- Pillow
- TkInter
- Caffe model (colorization_release_v2.caffemodel)

## Usage

### Command Line
To colorize an image using the command line:
```
python image_colarization.py
```
The script will process the image specified in the code and save the result as "result.png".

### Graphical Interface
To use the graphical interface:
```
python GUI.py
```
1. Click on "File" → "Upload Image" to select a black and white image
2. Click on "File" → "Color Image" to view the colorized result
3. The colorized image will be displayed side by side with the original

## Note
Before using the application, ensure you have downloaded the `colorization_release_v2.caffemodel` file and placed it in the `models/` directory.

## Examples
The repository includes several example images:
- Input black and white images: `new.jpg`, `new1.jpg`, `image.jpg`
- Output colorized images: `result.png`, `output.png`
