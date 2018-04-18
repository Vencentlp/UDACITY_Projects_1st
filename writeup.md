# **Finding Lane Lines on the Road** 


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

My pipeline consisted of 8 steps. 
(1)I selected the yellow and white color with a color filter. 
(2)I converted the images to grayscale.
(3)I applied Gaussian smoothing on the grayscle image to smooth out rough edges.
(4)I used cv2.Canny to find edges.
(5)I selected the reagon I was intetrested in by mask.
(6)I used hough transformation to detect lines in edge image.
(7)I drawed a single line on the left and right lanes by averaging all the lines' slopes and intercepts.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by adding calculation of the average slope and intercept for all the lines on both left and right sides and find four points to draw the left and right lines on the original image. 




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be the pipeline can not detect lane lines when there are shades on the line.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to add weights to the lanelines during color filter to make the detection robustly.
