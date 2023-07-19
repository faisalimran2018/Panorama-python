# Image Stitching for Panoramas in Python

This repository contains a script to create panoramic images using Python and OpenCV.

The script uses the SIFT (Scale Invariant Feature Transform) method for feature detection and description, and applies homography to stitch images together.

## How to Use

To use this script, simply pass the paths of the two images you want to stitch together when calling the script in your terminal:

```sh
python Image_Stitching.py '/path_to_your_image1.jpg' '/path_to_your_image2.jpg'
```

The script will then output a stitched image named 'final.jpg' in your current directory. 

Note: This script currently works with two images at a time. Ensure that both images are in the same directory as the script for easy access.

## Requirements

Before running the script, make sure you have the following Python libraries installed in your Python environment:

- OpenCV
- NumPy

You can install these using pip:

```sh
pip install opencv-python numpy
```

## Code Description

The script is made up of several functions within the `Image_Stitching` class:

- `registration(self,img1,img2)`: Performs feature matching between two input images.
- `create_mask(self,img1,img2,version)`: Creates a mask for blending the images.
- `blending(self,img1,img2)`: Applies the homography transformation matrix to stitch the images and blends them.
- `main(argv1,argv2)`: The main function that loads images, processes them, and saves the final stitched image.

Please ensure the compatibility of the OpenCV version with SIFT algorithm as it's patent protected and may not be included in some OpenCV distributions.

## Result
![image description](/Users/Faisal/PycharmProjects/pano/firstResult.jpg)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Thanks to OpenCV and its contributors for providing such a powerful library.
- Thanks to the open-source community for their continuous support.

## Disclaimer

This script is intended to be used for learning purposes. The author is not responsible for its use in any illicit activities or for any damages it might cause.

