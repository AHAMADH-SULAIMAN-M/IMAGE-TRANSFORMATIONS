# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules

### Step2:

Choose an image and save it as filename.jpg

### Step3:

Use imread to read the image

### Step4:

Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:

Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:

Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:

Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:

Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:

Crop the image to remove unwanted areas from an image

### Step10:

Use cv2.imshow to show the image

### Step11:

End the program

## Program:
```python
Developed By: AHAMADH SULAIMAN M
Register Number: 212224230009
i)Image Translation
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("mountains.webp")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")  
plt.axis('off')
#image translation
tx, ty = 100, 50  
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))  
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  
plt.title("Translated Image")  
plt.axis('off')

ii) Image Scaling

#scaled image
fx, fy = 5.0, 2.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  
plt.axis('off')

iii)Image shearing

#image shearing
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB)) 
plt.title("Sheared Image") 
plt.axis('off')

iv)Image Reflection

#Reflected image
reflected_image = cv2.flip(image, 2)  
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image") 
plt.axis('off')


v)Image Rotation
# Rotated Image
(height, width) = image.shape[:2] 
angle = 60 
center = (width // 2, height // 2) 
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image") 
plt.axis('off')



vi)Image Cropping

# cropped image
x, y, w, h = 100, 100, 200, 150  
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image") 
plt.axis('off')



```
## Output:
### i)Image Translation

<img width="702" height="478" alt="image" src="https://github.com/user-attachments/assets/da879115-6610-46f3-bd21-4c669f9ab523" />



### ii) Image Scaling

<img width="661" height="470" alt="image" src="https://github.com/user-attachments/assets/fe3ffa5a-f2ac-4a53-8d94-e42818977fe5" />



### iii)Image shearing

<img width="667" height="218" alt="image" src="https://github.com/user-attachments/assets/5a06c5f2-46b9-4f5b-83ae-d62dae82bbff" />



### iv)Image Reflection

<img width="644" height="519" alt="image" src="https://github.com/user-attachments/assets/e368f199-53d4-41e6-9f00-15c428c48517" />




### v)Image Rotation

<img width="653" height="464" alt="image" src="https://github.com/user-attachments/assets/7b734619-65ee-4796-9834-932424b1a019" />




### vi)Image Cropping

<img width="653" height="470" alt="image" src="https://github.com/user-attachments/assets/e1047088-415b-4a81-b0b9-0d3797ae7694" />





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
