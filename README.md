# WORKSHOP-3-Canny-Edge-Detection
# Aim
To implement the Canny Edge Detection algorithm on a sample image using Python and OpenCV to detect the edges present in the image.

# Objective
- Read a sample image.
- Reduce image noise using Gaussian Blur.
- Apply the Canny Edge Detection algorithm.
- Display the original, blurred, and edge-detected images.

# Software Requirements
- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook / VS Code / Google Colab

# Algorithm
The Canny Edge Detection process consists of the following major steps:
- Noise Reduction
Gaussian Blur is applied to reduce unwanted noise and small variations in the image.
- Gradient Calculation
The intensity gradients of the image are calculated to identify areas with significant intensity changes.
- Non-Maximum Suppression
Unnecessary pixels are removed to obtain thin and precise edges.
- Double Thresholding
Two threshold values are used to classify pixels as strong, weak, or non-edge pixels.
- Edge Tracking by Hysteresis
Weak edges connected to strong edges are retained, while isolated weak edges are removed.

# Program
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('saadhu.jpg',cv2.IMREAD_GRAYSCALE)
blurred =cv2.GaussianBlur(img, (5,5),0)
edges = cv2.Canny(blurred, 50, 150)
plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```

# Output


<img width="657" height="359" alt="image" src="https://github.com/user-attachments/assets/85ee9754-b7de-4a04-a0f8-2463f74761ed" />


# Result
The Canny Edge Detection algorithm was successfully implemented using OpenCV. The significant edges present in the sample image were detected after reducing image noise using Gaussian Blur.
