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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied GaussianBlur function after that I used 
canny edge detection function then I selected a region that contains the lane lines after that I applied hough transform then the last step was using the weighted function to draw the final image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 
-First I have calculated the slop of each line to detect if the line is left or right 
-After classifing the line the function calculates the line average for x and y as a point. 
-Each line position  is represented by a single average point.
-From all the right lines the functons chooses two points one represent the nearest line and the other represent the farest line
 and the same is applied for the left lines.
 -Multiple if condtions is added to handle special cases for lines.

If you'd like to include images to show how the pipeline works, here is how to include an image:



![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
