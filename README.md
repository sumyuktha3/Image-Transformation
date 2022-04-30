# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using

M=np.float32([[1,0,20],[0,1,50],[0,0,1]])

translated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step3:
Scale the image using

M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])

scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using

M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])

sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step5:
Reflection of image can be achieved through the code

M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step 6:
Rotate the image using

angle=np.radians(45)

M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])

rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step 7:
Crop the image using

cropped_img=input_img[20:150,60:230]


### Step 8:
Display all the Transformed images.

## Program:
### Developed By: S.Sumyuktha Rani
### Register Number: 212220230042

### i)Image Translation
```
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```
### ii) Image Scaling
```
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
### iii)Image shearing
```
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
```
### iv)Image Reflection
```
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
```
### v)Image Rotation
```
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
### vi)Image Cropping
```
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![sum1](https://user-images.githubusercontent.com/75235818/166112267-4241a662-02b5-49c8-8a18-b3c9f1c0aba7.jpg)

### ii) Image Scaling

![s2](https://user-images.githubusercontent.com/75235818/166112608-70058a06-4860-41f5-91fe-4eb8f7e2667b.jpg)

### iii)Image shearing

![s3](https://user-images.githubusercontent.com/75235818/166112606-b0e1995a-421f-4298-aa04-8f7be0aea2dc.jpg)

### iv)Image Reflection

![s5](https://user-images.githubusercontent.com/75235818/166112517-5ae5bff6-e1eb-43d7-ba08-8de9efc9b4cb.jpg)

### v)Image Rotation

![s6](https://user-images.githubusercontent.com/75235818/166112491-145a8c93-fc38-451e-bfb3-f75c6db66d4f.jpg)

### vi)Image Cropping

![s7](https://user-images.githubusercontent.com/75235818/166112387-f0899481-71c0-4da6-b076-efe57d951395.jpg)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
