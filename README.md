# Image-Transformation
## AIM:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image using<br>
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])<br>
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 3:
Scale the image using<br>
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])<br>
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 4:
Shear the image using<br>
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])<br>
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 5:
Reflection of image can be achieved through the code<br>
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])<br>
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 6:
Rotate the image using<br>
angle=np.radians(45)<br>
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])<br>
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 7:
Crop the image using <br>
cropped_img=input_img[20:150,60:230]
### Step 8:
Display all the Transformed images.
## PROGRAM:
```python
Developed By: Balaji N
Register Number: 212220230006
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("Dhoni.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation

![d1](https://user-images.githubusercontent.com/75235159/165504144-432587da-b99e-4a8f-884b-1ee7e33def35.JPG)


### ii) Image Scaling

![d2](https://user-images.githubusercontent.com/75235159/165504189-324feab0-390e-461e-9c6f-4b54ef55c275.JPG)


### iii)Image shearing
![d3](https://user-images.githubusercontent.com/75235159/165504232-e2765b94-1132-4e76-806e-f7cdd3a24a24.JPG)



### iv)Image Reflection
![d4](https://user-images.githubusercontent.com/75235159/165504269-6b8fb3db-8950-4112-a5e7-d1dd8cd4974c.JPG)


### v)Image Rotation
![d5](https://user-images.githubusercontent.com/75235159/165504289-f4d30c22-6caf-4f28-a2f5-94b10ef77d36.JPG)

### vi)Image Cropping
![d6](https://user-images.githubusercontent.com/75235159/165504336-bb6d7d2a-bce4-4a10-879e-136c0240629d.JPG)

## RESULT: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
