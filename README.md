# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

# Step1:
import the neccesary packages

# Step2:
create the text using cv2.put Text

# Step3:
create the structuting element

# Step4:
Erodde the image.

# Step5:
Dilate the image
 
## Program:

```

#NAME: Dharshini.S
#REG NO: 212224230061

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'DHARSH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


kernel = np.ones((3, 3), np.uint8)


eroded_image = cv2.erode(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

dilated_image = cv2.dilate(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

### Display the input Image

<img width="708" height="587" alt="image" src="https://github.com/user-attachments/assets/d6a9efbb-4722-49d6-a634-ad7ba24e1c11" />


### Display the Eroded Image

<img width="733" height="586" alt="image" src="https://github.com/user-attachments/assets/2b80a7f7-a68f-44f9-9296-1c185300db20" />

### Display the Dilated Image

<img width="702" height="593" alt="image" src="https://github.com/user-attachments/assets/66baa05f-90c1-46e1-a483-7bb61a593873" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
