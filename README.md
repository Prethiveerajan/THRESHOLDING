![gray7](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/b29515bd-f6c5-4b57-9f57-d33f474523e5)# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding, and Otsu's thresholding using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Import necessary packages

### Step2:
Read the image

### Step3:
If the read image is a color image, convert it into a grayscale image

### Step4:
perform the threshold operation you want to do(global thresholding or adaptive thresholding or otsu's 
thresholding)

### Step5:
Display the Results


## Program

```python
# Load the necessary packages

import cv2



# Read the Image and convert it to grayscale

img = cv2.imread('cat.jpeg',-1)
cv2.imshow('original_image',img)
cv2.waitKey(0)
cv2.destroyAllWindows
gray =cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('gray_image',gray)
cv2.waitKey(0)
cv2.destroyAllWindows


# Use Global thresholding to segment the image

ret,thresh_img1=cv2.threshold(gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(gray,100,255,cv2.THRESH_TRUNC)


# Use Adaptive thresholding to segment the image

thresh_img6=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img7=cv2.adaptiveThreshold(gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)


# Use Otsu's method to segment the image 

ret,thresh_img8=cv2.threshold(gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)



# Display the results

image =[thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
for i in range(0,8):
    cv2.imshow('threshold_image',image[i])
    cv2.waitKey(0)
    cv2.destroyAllWindows



```
## Output

### Original Image
![ori](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/822b40d9-68c5-44c3-bdb6-353d483484d5)


### Global Thresholding

![gray3](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/7ad61b23-7f3c-4db2-8ffc-6132fa02e521)

![gray5](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/1d55087a-9099-4702-bf1c-43ea6a58fd10)
![gray2](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/3fe49576-ac88-4ce7-9fca-e2d2cc7de98f)
![gray](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/eda1df4d-6638-4ad4-b5a9-16eaec0b1bfc)
![gray7](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/38399c98-02f7-42d2-ad03-664488592ee4)
![gray6](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/717765d9-09c6-43f5-aa9b-3fc646be4889)


### Adaptive Thresholding

![gray7](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/7515da24-9bba-4727-af75-d910a3dd3ae2)

![gray8](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/239f6e70-2a38-453d-9ef8-63f5b000860d)




### Optimum Global Thresholding using Otsu's Method
![gray9](https://github.com/Prethiveerajan/THRESHOLDING/assets/94233064/7a80ace7-6740-4e5f-84e2-851ec0e722c4)




## Result
Thus the images are segmented using global thresholding, adaptive thresholding, and optimum global thresholding using Python and OpenCV.

