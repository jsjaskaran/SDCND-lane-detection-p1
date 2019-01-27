# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

[//]: <> (My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... )

[//]: <> (In order to draw a single line on the left and right lanes, I modified the draw_lines function by ...)

[//]: <> (If you'd like to include images to show how the pipeline works, here is how to include an image:)

[//]: <> (![alt text][image1])

My pipeline consisted of following steps:
* Make a copy of image to perform all operations.
* Convert the image to grayscale image.
* Apply Gaussian blur along with Canny Edge Detection with selected threshold values.
* Find the region of interest which are the lane lines by giving fixed coordinates.
* Apply Hough transform to filter the edges.

***I applied this to all test images from test_images directory, you can find the output of these in the test_images_output directory***

***I also applied my pipeline to videos, you can find the output in test_videos_output directory***


### 2. Identify potential shortcomings with your current pipeline


[//]: <> (One potential shortcoming would be what would happen when ... )

[//]: <> (Another shortcoming could be ...)
- The first shortcoming is the hard coded coordinates for finding the lane lines. If the image is changed then this pipeline won't work.
- Second shortcoming would be that the lines are bit flickering, this could have smoothed out.


### 3. Suggest possible improvements to your pipeline

[//]: <> (A possible improvement would be to ...)

[//]: <> (Another potential improvement could be to ...)
- One improvement would be teach a machine to find lane lines in which I think deep learning especially CNN (Convolutional Neural Networks) would be helpful because they are used for image processing.
- Second would be to not have hard coded values of coordinates for finding lanes making it more general.
