# Python-Image-Upscaler with OpenCV and Numpy
A python image upscaler using different interpolation algorithms. I'm using OpenCV to read-write the image and Numpy to create an array of uint8 with the new image dimensions.

## Prerequisites
* **Python**
* **OpenCV**
* **Numpy**

## How to use
Give 3 arguments. A number to scale the image, the image's name and the interpolation technique. <br>
Here's an example: <br>

```python main.py 2 coffe.jpg bilinear``` <br>

This will save an image named *newcoffe.jpg* (you can change that in the code) two times larger with bilinear interpolation.

### Restraints:
Scale must be: **2 to MAXINT** (don't go big here :P). <br>
Image name: You could also give a full path, though you should change the save path in the code if so. <br>
Interpolation technique: **bilinear** or **nearest**, will do bicubic in the future.

If you get confused type ```python main.py -h``` for help.

## Examples
There are three step in bilinear. <br>
1. Map the pixels to your new image
2. Interpolate rows.
3. Interpolate columns.
![example](https://user-images.githubusercontent.com/49881189/95275496-4d77c480-0851-11eb-8871-a75ffc8254ca.png)
<br>

**Below you can see the differences between nearest neighbor and bilinear interpolation. In the *nearest* you get the color of the closest pixel, and in *bilinear* a rate of a pixel's color depending on how far away it is, hence the smoothing effect.**
![example2](https://user-images.githubusercontent.com/49881189/95272140-4ef0bf00-0848-11eb-8f5a-83d89df3c4ef.png)
<br>

## References
[Resizing Images - Computerphile](https://www.youtube.com/watch?v=AqscP7rc8_M) <br>
[Wikipedia - Bilinear Interpolation](https://en.wikipedia.org/wiki/Bilinear_interpolation)<br>
[Closest Neighbor Interpolation](https://www.imageeprocessing.com/2017/11/nearest-neighbor-interpolation.html)
