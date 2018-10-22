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

My pipeline consisted of 5 steps. First, I converted the images to grayscale,
-then I used  gaussian_blur funtion for smoothing
-then I used canny edge detection function to detect edges in the photo
-then I used region of interest function to take only the part of the photo that contains the lane lines
-after that I applied hough transform 
-the last thing was using weighted image function to draw the image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by:
-first I used slope to detect the right and left lanes
-for each line the function calculates the average of X and Y and gives a point represent average position for the line
-the function draws right line by using two points the first point represent the average position for the nearest right line
 the seconed represents the average position for the farest right line, I did the same for the left line.
-I have used multiple if conditions to handle the special cases.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]:
./examplesOutput/Lane1.jpg "Lane1"
./examplesOutput/Lane2.jpg "Lane2"
./examplesOutput/Lane3.jpg "Lane3"
./examplesOutput/Lane4.jpg "Lane4"
./examplesOutput/lane5.jpg "lane5"

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the position of lane lines differs may be in other images I think 
the output will not be accurate or correct.As I used the region of interest to cut images very close to lane lines.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to me be more robust model is better but i don't nw how to improve it

Another potential improvement could be to ...
