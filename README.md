# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By:
Register Number:
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
```
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)
```



iii)Image shearing
```
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image
```



iv)Image Reflection
```
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
```
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)
```




vi)Image Cropping
```
cropped_image=img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)
```






## Output:
### i)Image Translation
```
```

### ii) Image Scaling
```

```

### iii)Image shearing
<br>
<br>
<br>
<br>


### iv)Image Reflection
<br>
<br>
<br>
<br>



### v)Image Rotation
<br>
<br>
<br>
<br>



### vi)Image Cropping
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
