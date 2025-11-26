# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:
1.Translation moves the image along the x or y-axis. 2.Scaling resizes the image by scaling factors. 3.Shearing distorts the image along one axis. 4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.

## Program:
```python
Developed By:G Sanjay
Register Number:212224230243
```
## Function to display image using 
```
import cv2
import numpy as np
```
## Load the image
```
image = cv2.imread('boy.jpg') # Replace with your image path
(h, w) = image.shape[:2]
```

## i)Image Translation
## Move image 100 pixels right and 50 pixels down
```
tx, ty = 100, 50
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])
translated = cv2.warpAffine(image, translation_matrix, (w, h))
```
## iii)Image shearing
```
# Shear image horizontally
shear_matrix = np.float32([[1, 0.5, 0], [0, 1, 0]]) # x-shear
sheared = cv2.warpAffine(image, shear_matrix, (int(w + 0.5*h), h))
```
## iv)Image Reflection
## Flip horizontally (mirror image)
```
h_flip = cv2.flip(image, 1)
```
## Flip vertically
```
24
v_flip = cv2.flip(image, 0)
```
## v)Image Rotation
## Rotate by 45 degrees around the center
```
angle = 45
scale = 1.0
center = (w // 2, h // 2)
rotation_matrix = cv2.getRotationMatrix2D(center, angle, scale)
rotated = cv2.warpAffine(image, rotation_matrix, (w, h))
```
## vi) Image Cropping
```
# Crop a region (top-left 200x200)
cropped = image[0:200, 0:200]
```

## Output:
<img width="742" height="594" alt="image" src="https://github.com/user-attachments/assets/ea253a75-909e-40d4-9f35-423abc149df2" />

### i)Image Translation
<img width="748" height="596" alt="image" src="https://github.com/user-attachments/assets/a47d9cd0-6669-491b-b1e7-ea01acebbaf4" />

### ii) Image Scaling
<img width="806" height="327" alt="image" src="https://github.com/user-attachments/assets/4800ab43-b1a4-4630-a851-677cf7285839" />

### iii)Image shearing
<img width="819" height="460" alt="image" src="https://github.com/user-attachments/assets/8fd8bc89-2076-4fce-8243-e0f800891570" />

### iv)Image Reflection
<img width="739" height="603" alt="image" src="https://github.com/user-attachments/assets/05e296f4-b019-4263-9145-d1b1602bede2" />

<img width="743" height="608" alt="image" src="https://github.com/user-attachments/assets/12dd93a5-7740-4d49-b18b-f22144640f62" />

### v)Image Rotation
<img width="744" height="603" alt="image" src="https://github.com/user-attachments/assets/790c16fb-9aee-4161-bead-a5587ad19434" />

### vi)Image Cropping
<img width="311" height="347" alt="image" src="https://github.com/user-attachments/assets/96b62d56-e235-4989-8691-44a4479f7fe6" />

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
