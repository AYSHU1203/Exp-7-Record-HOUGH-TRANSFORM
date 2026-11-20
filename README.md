# Exp-7-Record-HOUGH-TRANSFORM
## NAME: AYSHWARIYA J
## REG NO:212224230030


##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

```python 

import cv2

import numpy as np

import matplotlib.pyplot as plt

image = cv2.imread('Qno.1.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))

plt.title("Input Image")

plt.axis('off')

plt.imshow(gray_image, cmap='gray')

plt.title("Grayscale Image")

plt.axis('off')

edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(edges, cmap='gray')

plt.title("Canny Edge Detector")

plt.axis('off')

lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)

for line in lines:
    x1, y1, x2, y2 = line[0]  
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))

plt.title("Result of Hough Transform")

plt.axis('off')

```

##  Expected Output

* Original image

<img width="648" height="625" alt="image" src="https://github.com/user-attachments/assets/4ffd9ff4-61e2-4fc1-b50c-f9ad41814b3b" />


* Grayscale image

<img width="631" height="627" alt="image" src="https://github.com/user-attachments/assets/8b712791-71d8-4dcb-8233-803bca758470" />


* Canny Edge Detector

<img width="642" height="630" alt="image" src="https://github.com/user-attachments/assets/38bd3071-d392-4684-abe3-4c0cbe6dfe95" />



* Final Hough Transform

<img width="641" height="633" alt="image" src="https://github.com/user-attachments/assets/06045c12-c856-44e1-b11f-dd655b55d785" />


---


## Result

Thus, the Hough Transform  is successfully implemented by completing the missing code sections. The system detects and highlights hough transform effectively.

---

##  Developed By

* **Name:** AYSHWARIYA J
* **Register No:** 212224230030
