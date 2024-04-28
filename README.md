# Seyed CV

this repository contains some of my linear algebra projects that i gather them here.


# part 1: SeyedCV
seyedCV is a class that edits images using linear algebra methods.

here is it's functionality:

## 1. Resize Operation:
### Concept: Scaling Transformation
**Explanation**: The resize operation rescales the image by applying a scaling transformation. It achieves this by creating a grid of coordinates in the output image and applying the inverse transformation to these coordinates. The coordinates are divided by the scaling factors, resulting in a rescaled image. The rounding of coordinates ensures that the nearest pixel in the input image is obtained.
#### matrix:

\begin{bmatrix}
sx & 0 \\
0 & sy \\
\end{bmatrix}

![resize12](ans/resize12.png)
![resize21](ans/resize21.png)
## 2. Rotate Operation:
### Concept: Rotation Transformation
**Explanation**: The rotate operation rotates the image by applying a rotation transformation. It begins by converting the rotation angle to radians. A grid of coordinates is then created in the output image. The coordinates are centered by subtracting the width and height of the image by 2. The inverse rotation transformation is applied to these coordinates using trigonometric functions. The shifted and rounded coordinates are then used to index the input image, resulting in a rotated image.
#### matrix:

\begin{bmatrix}
cos($\theta$) & -sin($\theta$) \\
sin($\theta$) & cos($\theta$) \\
\end{bmatrix}

![rotated image](ans/rotate.png)
# 3. Sobel Filter Operation:
## Concept: Convolution
**Explanation**: The sobel_filter operation applies a convolution operation to the image using a specific filter. Convolution involves element-wise multiplication of the filter and the image, followed by summing the results. This operation is a linear transformation in linear algebra. The sobel_filter operation utilizes a 3x3 filter matrix to detect edges in the image.
### matrix:
\begin{bmatrix}
-1 & -2 & -1 \\
0 & 0 & 0 \\
1 & 2 & 0 \\
\end{bmatrix}

![sobel filter](ans/sobel.png)
# 4. Prewitt Filter Operation:
## Concept: Convolution
**Explanation**: The prewitt_filter operation also applies a convolution operation to the image using a specific filter. Similar to the sobel_filter operation, it involves element-wise multiplication of the filter and the image, followed by summing the results. This operation is a linear transformation in linear algebra. The prewitt_filter operation utilizes a 3x3 filter matrix to detect edges in the image.
### matrix:
\begin{bmatrix}
-1 & 0 & 1 \\
-1 & 0 & 1 \\
-1 & 0 & 1 \\
\end{bmatrix}

![prewitt](ans/prewitt.png)
# 5. Sharpen Filter Operation:
## Concept: Convolution
**Explanation**: The sharpen_filter operation applies a convolution operation to the image using a specific filter. It involves element-wise multiplication of the filter and the image, followed by summing the results. This operation is a linear transformation in linear algebra. The sharpen_filter operation utilizes a 3x3 filter matrix to enhance the sharpness of the image.
### matrix:
\begin{bmatrix}
0 & -1 & 0 \\
-1 & -5 & -1 \\
0 & -5 & 0 \\
\end{bmatrix}

![sharpen](ans/sharpen.png)
# 6. Blur Filter Operation:
## Concept: Convolution
**Explanation**: The blur_filter operation applies a convolution operation to the image using an averaging filter. Similar to the previous operations, it involves element-wise multiplication of the filter and the image, followed by summing the results. This operation is a linear transformation in linear algebra. The blur_filter operation utilizes a 5x5 averaging filter matrix to blur the image.
### matrix:
\begin{bmatrix}
\frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} \\
\frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} \\
\frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} \\
\frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} \\
\frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} & \frac{1}{25} \\
\end{bmatrix}

![blur](ans/blur.png)
# 7. Invert Color Operation:
## Concept: Linear Transformation
**Explanation**: The invert_color operation applies a linear transformation to each pixel of the image. It subtracts the pixel value from 255 to invert the color. This operation is a linear transformation in linear algebra.
### metrix: Please note that these are not matrices in the linear algebra sense, but rather operations applied to each pixel in the image.
```
R' = 255 - R
G' = 255 - G
B' = 255 - B
```

![invert color](ans/invert.png)
# 8. Luminosity Operation:
## Concept: Linear Transformation
**Explanation**: The luminosity operation applies a linear transformation to each pixel of the image. It calculates the luminosity value of each pixel using a weighted sum of the RGB values. This operation is a linear transformation in linear algebra.
### matrix:
\begin{bmatrix}
0.2989 & 0.5870 & 0.1140 \\
\end{bmatrix}

![luminosity](ans/luminosity.png)
# 9. Color Balance Operation:
## Concept: Linear Transformation
**Explanation**: The color_balance operation applies a linear transformation to each pixel of the image. It multiplies the RGB values of each pixel by the specified color balance factors and clips the result to the valid range. This operation is a linear transformation in linear algebra.
### matrix:
\begin{bmatrix}
red scale & green scale & blue scale \\
\end{bmatrix}

![color balance](ans/balance.png)
## 10. comprassion:
**Explanation**: This is achieved by dividing the pixel values of the image by 4 and then multiplying them by 4, effectively reducing the color depth to a quarter of its original value. This method is a simple form of quantization, which can significantly reduce the file size of an image at the cost of some loss in image quality.
![compress](ans/compress.png)