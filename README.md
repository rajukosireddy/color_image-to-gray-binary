# color_image-to-gray&binary
This Python script showcases basic image processing techniques using the OpenCV library. It reads an input color image, converts it to grayscale, applies binary thresholding, and displays the results. The script serves as a practical example for those interested in understanding simple image manipulation with OpenCV.

## Table of contents

- [Features](#features)
- [Dependencies](#dependencies)
- [Acknowledgments](#acknowledgments)
- [Code Explanation](#code-explanation)
- [Input-color-Image](#input-color-image)
- [Gray-Image](#gray-image)
- [Binary-Image](#binary-image)
  
## Features:
1. Color Image Display: Visualize the original color image.
2. Grayscale Conversion: Convert the color image to grayscale for further analysis.
3. Binary Thresholding: Apply binary thresholding to segment the grayscale image.
4. User-friendly: Easy-to-understand code structure, suitable for beginners in image processing.

## Dependencies:
Ensure you have the required dependencies installed:
1. Python
2. OpenCV

## Acknowledgments:
1. OpenCV community for the powerful image processing library.
2. Google Colab for providing a convenient environment for running Python scripts.

## Code Explanation:

The code is divided into the following sections:

- `cv2`: OpenCV library for computer vision and image processing.
- `cv2_imshow`: A function provided by Google Colab to display images.
  ```bash
  import cv2
  from google.colab.patches import cv2_imshow
  ```
- Read a color image from the file '1704113778755.png' using cv2.imread().
- The cv2.IMREAD_COLOR flag indicates that the image should be loaded in color.
  ```bash
  color_img = cv2.imread('/content/1704113778755.png', cv2.IMREAD_COLOR)
  ```
  
- Check if the image has been successfully loaded. If so, display the original color image using cv2_imshow().
  ```bash
  if color_img is not None:
    cv2_imshow(color_img)
  ```
  
- Convert the color image to grayscale using cv2.cvtColor() with the cv2.COLOR_BGR2GRAY conversion. Display the grayscale image.
  ```bash
      gray_img = cv2.cvtColor(color_img, cv2.COLOR_BGR2GRAY)
      cv2_imshow(gray_img)
  ```
  
- Apply binary thresholding to the grayscale image using cv2.threshold().
- Pixels with intensity greater than 127 are set to 255 (white), and others to 0 (black). Display the binary image.
  ```bash
      _, binary_img = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
      cv2_imshow(binary_img)

- Obtain the number of rows and columns in the color image using shape[:2] and print the results.
  ```bash
      rows, cols = color_img.shape[:2]
      print(f'Number of rows: {rows}')
      print(f'Number of columns: {cols}')
  ```

- If there is an issue loading the image (e.g., file not found), print an error message.
  ```bash
  else:
    print('Error loading the image.')
  ```

- The code provides a basic image processing example, displaying the original color image, its grayscale version, and the result of binary thresholding. It's designed to be run in a Google Colab environment, hence the use of cv2_imshow() for image display.

## Input-color-Image:

![color_image](https://github.com/rajukosireddy/color_image-to-gray-binary/assets/141699777/a3857f03-2ff5-4134-85a1-552a91c93e5c)

## Gray-Image:

![image](https://github.com/rajukosireddy/color_image-to-gray-binary/assets/141699777/c04a21be-a2d0-4ac4-8bab-e00727012c40)

## Binary-Image:

![image](https://github.com/rajukosireddy/color_image-to-gray-binary/assets/141699777/9450298c-328e-44bc-82f4-774281377ed6)


# Rows & Columns:
- Number of rows: 4192
- Number of columns: 3144


  


    
