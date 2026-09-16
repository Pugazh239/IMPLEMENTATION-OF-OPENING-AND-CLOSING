# IMPLEMENTATION-OF-OPENING-AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
**Step-1:**

Import the necessary packages

**Step-2:**

Create the Text using cv2.putText

**Step-3:**

Create the structuring element

**Step-4:**

Use Opening operation

**Step-5:**

Use Closing Operation

 
## Program:
```
Developed by: Pugazh sozhan.A
Reg.No: 212224240121
```

~~~
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the image
image = cv2.imread("images10.JPEG")

# Check if image is loaded
if image is None:
    print("Error: Image not found")
else:
    # Step 2: Convert BGR to RGB
    image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

    # Step 3: Create a structuring element (5x5 rectangular)
    kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

    # Step 4: Perform Morphological Opening
    opening = cv2.morphologyEx(image_rgb, cv2.MORPH_OPEN, kernel)

    # Step 5: Perform Morphological Closing
    closing = cv2.morphologyEx(image_rgb, cv2.MORPH_CLOSE, kernel)

    # Step 6: Plot the images
    plt.figure(figsize=(10, 5))

    plt.subplot(1, 3, 1)
    plt.imshow(image_rgb)
    plt.title("Original Image")
    plt.axis("off")

    plt.subplot(1, 3, 2)
    plt.imshow(opening)
    plt.title("Opening")
    plt.axis("off")

    plt.subplot(1, 3, 3)
    plt.imshow(closing)
    plt.title("Closing")
    plt.axis("off")

    plt.tight_layout()
    plt.show()
~~~

Output:

<img width="990" height="270" alt="download" src="https://github.com/user-attachments/assets/5e9a7ad9-e721-4f10-a5fe-9e05a81da130" />


Result:

Thus,the Opening and Closing operation is used in the image using python and OpenCV.









