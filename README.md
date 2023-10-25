# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it
### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np


# Create the Text using cv2.putText

img= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'M.PRAKASH',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element



# Erode the image

erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Dilate the image


dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image

<img width="913" alt="image" src="https://github.com/Prakashmathi2004/EROSION-AND-DILATION/assets/118350045/70da9ac4-55f2-4766-9c80-19f118ad8d38">



### Display the Eroded Image

<img width="902" alt="image" src="https://github.com/Prakashmathi2004/EROSION-AND-DILATION/assets/118350045/ecbf1466-31ab-4cbd-b5cd-81fb97389bb7">

<img width="923" alt="image" src="https://github.com/Prakashmathi2004/EROSION-AND-DILATION/assets/118350045/9b60136d-2697-49f1-b02d-27bb0170de41">

### Display the Dilated Image

<img width="928" alt="image" src="https://github.com/Prakashmathi2004/EROSION-AND-DILATION/assets/118350045/6ef74aa8-1e0d-4b69-b7b4-fcc5b290a81c">

<img width="924" alt="image" src="https://github.com/Prakashmathi2004/EROSION-AND-DILATION/assets/118350045/00001e96-9b6d-4741-9531-a257220ed12f">


## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.
