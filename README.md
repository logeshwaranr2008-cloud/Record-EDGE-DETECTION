## Record-EDGE-DETECTION

## Exp: No: 6: Edge-detection-opencv

## Aim:
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

## Software Required:
* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## ⚙️ Algorithm:

## Step 1:
Import all the necessary modules for the program.

## Step 2:
Load an image using cv2.imread().

## Step 3:
Convert the image to grayscale.

## Step 4:
Apply Sobel operator using OpenCV to detect edges.

## Step 5:
Apply Prewitt operator using custom kernels.

## Step 6:
Apply Roberts operator using custom kernels.

## Step 7:
Apply Laplacian operator using OpenCV.

## Step 8:
Apply Canny edge detector using OpenCV.

## Step 9:
Display all edge-detected images for comparison.

## Program:

## Developed By: LOGESHWARAN R

## Register No: 212225040205

## Original Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('sai1.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

## Sobel Edge Detection:

```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y) 
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

## Laplacian Edge Detection:

```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

## Canny Edge Detection:

```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```


## Output:

## Original Image:

<img width="216" height="405" alt="image" src="https://github.com/user-attachments/assets/7be4dc2d-e98a-4f05-ac42-d64353e9efe0" />

## Sobel Edge Detection:

<img width="232" height="412" alt="image" src="https://github.com/user-attachments/assets/cfc4c7df-85f3-48bc-86d7-c19a9fe91892" />

## Laplacian Edge Detection:

<img width="262" height="406" alt="image" src="https://github.com/user-attachments/assets/d0abc3aa-1db0-4bc7-b16b-b98a1b6a5cbe" />

## Canny Edge Detection:

<img width="225" height="420" alt="image" src="https://github.com/user-attachments/assets/b800be4f-e052-4ee6-baed-d37672988feb" />

## Result:
Thus, edges are successfully detected using Sobel, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
