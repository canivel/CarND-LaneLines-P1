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
	 1) converted the images to grayscale 
	 2) apply gaussian 
	 3) define Canny and apply 
	 4) define the vertices to mask 
	 5) mask the edges 
	 6) define the Hough transform and run it on edge detected image
	In order to draw a single line on the left and right lanes, I modified the draw_lines() function by: 
	 1)Find the left and right lines and group them 
	 2)Find the slope and intercept averages 
	 3)calculate min and max of X 4)draw it

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when resolution is bad because of weather like fog for example, 
curves will fail, and probably will need a higher fps camera to stop the flikering.


### 3. Suggest possible improvements to your pipeline

High FPS camera, for better transition between imagens will have better results Tunning the parameters, 
like create a simple model for training and apply a some kind of gridsearch to it.