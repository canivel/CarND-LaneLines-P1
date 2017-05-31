# **Finding Lane Lines on the Road** 

## Writeup 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


My pipeline consisted of 6 steps explained in the past lessons:
* converted the images to grayscale 
* apply gaussian 
* define Canny and apply 
* define the vertices to mask 
* mask the edges 
* define the Hough transform and run it on edge detected image

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by: 
* Find the left and right lines and group them 
* Find the slope and intercept averages 
* calculate min and max of X 
* draw the line

### 2. Identify potential shortcomings with your current pipeline


Some of the potential fails would be:
* if the image resolution is bad because of weather like with fog, shadowns, for example, the algo does not have any noise reduction filter for that 
* curves will fail
* tree shadows or another car changing lanes right in front of our car

### 3. Suggest possible improvements to your pipeline

* High FPS camera, for better transition between imagens will have better results
* Tunning the parameters.
* modify the image mask to limit the detection range
* limit the slope value to avoid jitter lines
* only search for white and yellow lines
