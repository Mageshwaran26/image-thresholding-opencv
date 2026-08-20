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

**Name:** Mageshwaran T.A

**Register No:** 212224230146

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
<img width="473" height="522" alt="image" src="https://github.com/user-attachments/assets/9df96033-637b-43c4-9545-864998a1fa02" />

~~~
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lego.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
~~~

<img width="494" height="504" alt="image" src="https://github.com/user-attachments/assets/355d33a6-184c-4ef2-aef2-1d6943c95d04" />

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

<img width="542" height="510" alt="image" src="https://github.com/user-attachments/assets/59418527-c870-45d7-8adc-15a4cbdc4991" />

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

<img width="498" height="507" alt="image" src="https://github.com/user-attachments/assets/bbb42052-7b1d-4034-a99f-0147731d30c6" />

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
<img width="483" height="509" alt="image" src="https://github.com/user-attachments/assets/b2f18eae-7ffa-4afe-a1e8-853102ac0bab" />

## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
