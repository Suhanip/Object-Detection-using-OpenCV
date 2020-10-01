# Object-Detection-using-OpenCV
This is an custom object detection project using OpenCV.

The object that is considered here is "Strawberry :strawberry:".

### The functions used:
 - _show(image)_ : this is used to show the new image in which our object is detected.
 - _overlay(mask, image)_ : this function is used to create the overlay for the image by adding the weights of the masks with the weights of the image.
 - _find_biggest_contour(image)_: this function is used to find the biggest strawberry from all present in the image.
 - _circle_contour(image, contour)_ : this function is used for defining the size of the ellipse (around the image detected).
 - _find_strawberries(image)_: This is the main function to detect the strawberries in the given image.

### Steps involved:
1. Convert to correct colour scheme from BGR to RGB by using cvtColor().This is done because when any transformation is done on the image, it follows some particular color schema.
2. Convert to correct size using resize().This will give a square image (fx=fy).
3. Clean the image using GaussianBlur().
4. Define the filter for the image. Here we have used two filters:
   - filter by colours
   - filter by brightness
5. segmentation(use masks to separate the strawberries from other)
6. Find biggest strawberry
7. Overlay mask that we created on our image
8. Circle the biggest strawberry
9. Convert back to original color scheme

### Output:
<img src="https://github.com/Suhanip/Object-Detection-using-OpenCV/blob/master/original_image.jpg" width=200px height=200px><img src="https://github.com/Suhanip/Object-Detection-using-OpenCV/blob/master/detected_image.PNG" width=200px height=200px>
