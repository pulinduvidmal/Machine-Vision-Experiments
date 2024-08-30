## Introduction

This code demonstrates the application of various linear and non-linear filters to remove noise from images. Specifically, it targets the removal of salt-and-pepper noise, which is characterized by random black and white pixels.

The filters applied include:
- **Linear Filters**: Box Filter, Weighted Filter, Gaussian Filter
- **Non-Linear Filters**: Min Filter, Max Filter, Median Filter

## Filters Implemented

### Linear Filters

1. **Box Filter (Mean Filter):**
   - Averages pixel values within a kernel to reduce noise.
   - Effective for general smoothing but may blur edges.

2. **Weighted Filter (Normalized Box Filter):**
   - A general form of convolutional filter where each pixel in the kernel has a weight.
   - The weights are normalized (sum to 1) for better balance between smoothing and edge preservation.

3. **Gaussian Filter:**
   - A weighted filter with weights following a Gaussian distribution.
   - Preserves edges better than the box filter while reducing noise.

### Non-Linear Filters

1. **Min Filter (Erosion):**
   - Replaces each pixel with the minimum value in the kernel.
   - Removes small white noise but can shrink image features.

2. **Max Filter (Dilation):**
   - Replaces each pixel with the maximum value in the kernel.
   - Removes small black noise but can expand image features.

3. **Median Filter:**
   - Replaces each pixel with the median value of surrounding pixels.
   - Highly effective at removing salt-and-pepper noise without blurring edges.



