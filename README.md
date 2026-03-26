# Implementation-of-Erosion-and-Dilation

#DEVELOPED BY :Susindhar K M
#REG NO : 212223040218
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.


### Step2:
Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.

### Step3:
Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.

### Step4:
Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.

### Step5:
Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.

### Step6:
Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.

### Step7:
Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.


 
## Program:
Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype="uint8")
Create the Text using cv2.putText
text = "M.Suren."
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
Original image
```
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```
Dilate the image

```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```

## Output:

### Display the input Image
<img width="512" height="534" alt="Screenshot 2026-03-26 135050" src="https://github.com/user-attachments/assets/0055b8a8-f8e3-46aa-a8b1-65985fc218d6" />


### Display the Eroded Image
<img width="500" height="523" alt="Screenshot 2026-03-26 135058" src="https://github.com/user-attachments/assets/cebe70f8-e011-4bdd-8e27-da00c123f2b9" />


### Display the Dilated Image
<img width="492" height="530" alt="Screenshot 2026-03-26 140627" src="https://github.com/user-attachments/assets/04f031f4-c21c-4317-a180-1351ef3d0084" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
