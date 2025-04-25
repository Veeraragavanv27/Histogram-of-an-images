# Histogram of an images

## Aim

To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Read the gray and color image using imread()

### Step 2:
Print the image using imshow().

### Step 3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step 4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step 5:
The Histogram of gray scale image and color image is shown.


## Program :

## Developed By : Veeraragavan V
## Register Number : 212223230237

## Input Grayscale Image :
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('image.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```

## Histogram of Grayscale Image :

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```

## Equalization :

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```

## Equalized Histogram :

```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```






## Output:

### Input Grayscale Image and Color Image

![Screenshot 2025-04-25 202923](https://github.com/user-attachments/assets/47847b99-ef59-41db-8c8f-dceeece6d3b9)


### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2025-04-25 202935](https://github.com/user-attachments/assets/6a19ec90-6e59-4f8a-92a7-becb540ef0e2)


### Histogram Equalization of Grayscale Image.
![Screenshot 2025-04-25 202945](https://github.com/user-attachments/assets/c7582763-d2aa-4ad6-af52-60a31b8d3fca)


### Equalized Histogram. 
![Screenshot 2025-04-25 202954](https://github.com/user-attachments/assets/961029a0-c03b-435b-9ea4-8afaf39d0eaa)


## Result: 

Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
