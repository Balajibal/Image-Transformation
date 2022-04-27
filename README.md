# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
```
Import the necessary libraries and read the original image and save it a image variable.
```

### Step2:
```Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))```

### Step3:
```
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
```

### Step4:
```
Shear the image using

Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))
```


### Step5:
```
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
```

### Step6:
```
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
```

### Step7:
```
Crop the image using cropped_image=org_img[10:350,320:560]
```

### Step8:
```
Display all the Transformed images.
```


## Program:
```python
Developed By: BALAJI N
Register Number: 212220230006
i)Image Translation
import cv2
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread("build.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(img)
row,col,dim=img.shape
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)
```

ii) Image Scaling
```python
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)
```



iii)Image shearing
```python
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image
```



iv)Image Reflection
```python
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)
Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)
```



v)Image Rotation
```python
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)
```




vi)Image Cropping
```python
cropped_image=img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)
```






## Output:
### i)Image Translation

![Screenshot (115)](https://user-images.githubusercontent.com/75234946/165560392-9ca27b85-7524-4df1-9b16-133a11e4a215.png)


### ii) Image Scaling

![Screenshot (116)](https://user-images.githubusercontent.com/75234946/165560642-47322aec-eb35-4aaf-b705-1be7b6012009.png)


### iii)Image shearing

![Screenshot (117)](https://user-images.githubusercontent.com/75234946/165563357-879d34ff-1ca9-495f-bb78-fcaa78f22595.png)


### iv)Image Reflection

![Screenshot (110)](https://user-images.githubusercontent.com/75234946/165559026-5b1bfec7-7ea7-4e46-82af-3e2b28784a64.png)



### v)Image Rotation

![Screenshot (111)](https://user-images.githubusercontent.com/75234946/165559148-927193d4-e24a-4d6a-aafd-aee5476c6cdc.png)




### vi)Image Cropping

![Screenshot (112)](https://user-images.githubusercontent.com/75234946/165559442-4b8b87c8-392a-42f9-ae83-edbee93e8e18.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
