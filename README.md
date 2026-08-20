# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** JEEVAN IRUDHAYAM L

**Register No:** 26014247

## Output

### Original Grayscale Image
~~~
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
~~~
<img width="295" height="502" alt="Screenshot 2026-08-20 172227" src="https://github.com/user-attachments/assets/27059f8b-f693-4c7c-a4cf-26d8a0cdbe3e" />


~~~
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
~~~

 <img width="289" height="504" alt="Screenshot 2026-08-20 172309" src="https://github.com/user-attachments/assets/7393b98b-6062-4f9e-8a9c-6dafa25838f5" />


~~~
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
~~~

<img width="323" height="492" alt="Screenshot 2026-08-20 172324" src="https://github.com/user-attachments/assets/dafdc8bd-fc54-4802-b19c-646d34e41776" />


~~~
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
~~~
<img width="301" height="528" alt="Screenshot 2026-08-20 172348" src="https://github.com/user-attachments/assets/fbe81b70-6949-441a-86fc-552824cec2dd" />

~~~

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
~~~
<img width="276" height="512" alt="Screenshot 2026-08-20 172407" src="https://github.com/user-attachments/assets/266b205c-b552-4555-af09-048fe63b143a" />

## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
