# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
1. Import the necessary packages to do Erosion and Dilution.


### Step2:
2. Create the text image of our name using putText from cv2 package.

### Step3:
3. Create the required structural element.

### Step4:
4. Apply Erode and Dilution for our NameImage
### Step5:
5. Display the output images.
### step6:
6. End the program.
 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy


# Create the Text using cv2.putText

NameImage = numpy.zeros((100,1000),dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(NameImage,'vivek',(50,70),font,2,(255),5,cv2.LINE_4)
cv2.imshow("Name Image",NameImage)



# Create the structuring element

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))



# Erode the image

erodeImage = cv2.erode(NameImage,kernel1)



# Dilate the image


dilationImage = cv2.dilate(NameImage,kernel1)

# Displaying the image
cv2.imshow("Name Image",NameImage)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
~~~
## Output:

### Display the input Image
![vi1](https://user-images.githubusercontent.com/94525701/174118378-a755c82d-c3e6-4015-984d-80e80089b22f.jpeg)

### Display the Eroded Image
![vi2](https://user-images.githubusercontent.com/94525701/174118410-a77f948d-503b-467e-b943-f04d54632b86.jpeg)

### Display the Dilated Image
![vi3](https://user-images.githubusercontent.com/94525701/174118469-4958bb7b-8ca3-487c-a396-96aceef0b4db.jpeg)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
