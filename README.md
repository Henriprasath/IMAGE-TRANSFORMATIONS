# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

Step2:
Read the input image using cv2.imread() and store it in a variable for further processing

Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis. 2.Scaling resizes the image by scaling factors. 3.Shearing distorts the image along one axis. 4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

## Program:
```python
Developed By: HENRIPRASATH S
Register Number: 212223230077
```
```
i)Original Image:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread('chep.jpg')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Original Image")  
plt.axis('off')

ii)Image Translation:

tx, ty = 200, 100
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  # Display the translated image
plt.title("Translated Image")  
plt.axis('off')

iii) Image Scaling:

fx, fy = 1.0, 3.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  # Set title
plt.axis('off')

iv)Image shearing:

shear_matrix = np.float32([[1, -0.5, 0], [-0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB)) 
plt.title("Sheared Image")  
plt.axis('off')

v)Image Reflection:

reflected_image = cv2.flip(image, 2)
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB)) 
plt.title("Reflected Image") 
plt.axis('off')

vi)Image Rotation:

image = cv2.imread('bean.jpg')
(h, w) = image.shape[:2]
M = cv2.getRotationMatrix2D((w // 2, h // 2), 45, 1)
rotated = cv2.warpAffine(image, M, (w, h))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))
plt.title("Rotated Image")
plt.axis('off')

vii)Image Cropping:

x, y, w, h = 150, 150, 300, 100
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))
plt.title("Cropped Image") 
plt.axis('off')

```

## Output:

### i)Original Image:

![Screenshot 2025-04-30 014109](https://github.com/user-attachments/assets/4934be50-1e25-431b-b5f0-14c31548a6e1)


### ii)Image Translation

![Screenshot 2025-04-30 014117](https://github.com/user-attachments/assets/b8913465-ef65-4295-a30e-4c3659318ee5)


### iii) Image Scaling

![Screenshot 2025-04-30 014123](https://github.com/user-attachments/assets/ce4e09f1-5e17-450d-823e-ba5a5e99d3f3)


### iv)Image shearing

![Screenshot 2025-04-30 014131](https://github.com/user-attachments/assets/959c6bba-84c9-4cf5-8cfa-61ea70826e3f)


### v)Image Reflection

![Screenshot 2025-04-30 014138](https://github.com/user-attachments/assets/f7fc02e4-088b-41e0-9aee-16e09ba9840c)


### vi)Image Rotation

![Screenshot 2025-04-30 014144](https://github.com/user-attachments/assets/da781224-7945-4f73-a5c4-4ca15388080d)


### vii)Image Cropping

![Screenshot 2025-04-30 014149](https://github.com/user-attachments/assets/e025dae7-4f1b-42ef-8914-36004b2a8e93)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
