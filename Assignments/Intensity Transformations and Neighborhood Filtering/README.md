# Implement the intensity transformation

```python

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the image
image = cv2.imread('emma.jpg', 0)  # Grayscale

# Define the intensity transformation as a function
def intensity_transform(pixel_value):
    # Example transformation based on Fig. 1a
    return 255 * (pixel_value / 255) ** 0.5  # Gamma correction with γ=0.5

# Apply the transformation
transformed_image = np.array([intensity_transform(pixel) for pixel in image.flatten()]).reshape(image.shape)

# Display the result
plt.imshow(transformed_image, cmap='gray')
plt.show()

```
