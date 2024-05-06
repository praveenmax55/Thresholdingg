
# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Install the opencv in the jupiter notebook
### Step2:
Import cv2 and numpy
### Step3:
Read the image by cv2.read(
### Step4:
Doing the global Global Thresholding,Adaptive Thresholding,Otsu's Thresholding 
### Step5:
By using opencv module show the image by running the programm.
## Program
# Developed by: Praveen D
# Register number: 212222240076
# Load the necessary packages:
```
import cv2
import numpy as np
```



# Read the Image and convert to grayscale
```
image = cv2.imread('username.jpg', 0)
```


# Use Global thresholding to segment the image

```
_, global_thresh = cv2.threshold(image, 127, 255, cv2.THRESH_BINARY)
```


# Use Adaptive thresholding to segment the image


```
adaptive_thresh = cv2.adaptiveThreshold(image, 255, cv2.ADAPTIVE_THRESH_MEAN_C, cv2.THRESH_BINARY, 11, 2)
```

# Use Otsu's method to segment the image 

```
_, otsu_thresh = cv2.threshold(image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```


# Display the results
```
cv2.imshow('Original Image', image)
cv2.imshow('Global Thresholding', global_thresh)
cv2.imshow('Adaptive Thresholding', adaptive_thresh)
cv2.imshow("Otsu's Thresholding", otsu_thresh)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output

### Original Image
![image](https://github.com/praveenmax55/Thresholdingg/assets/113497509/45be211e-739f-400c-a6a2-1538d91977b2)


### Global Thresholding
![image](https://github.com/praveenmax55/Thresholdingg/assets/113497509/4b767eb9-637b-4b0d-a751-7e2b77ed04ca)


### Adaptive Thresholding
![image](https://github.com/praveenmax55/Thresholdingg/assets/113497509/8b1421c4-57c3-4e4c-84a0-32eb189336a8)


### Optimum Global Thesholding using Otsu's Method
![image](https://github.com/praveenmax55/Thresholdingg/assets/113497509/269887c2-09bd-494c-92e7-b8eb17021ce7)



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
