# **Finding Lane Lines on the Road**

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

**Reflection**

## Description

### 1. Pipeline consists of following steps
- **grayscale:** converts an image to grayscale
- **gaussian_blur:** applies gaussian blur to an image
- **canny:** finds the edges of an image using canny edge detection
- **region_of_interest:** masks an image inside a polygon. All the pixels outside the polygon are converted to black.
- **hough_lines:** finds the lines of an image using hough transform
- **get_dist:** calculate distance between two points
- **get_full_line:** make a 220 pixels length line according to the initial line's slope
- **draw_lines:** draws the two lane lines
- **weighted_img:** plots the lines on the original image

### 2. Modification of draw_lines()
- I imagine that each image has two equal parts: left and right
- Left lane line is located in the left part and right lane line is located in the right part
- First, I find the longest line that is located in the left part of the image. I assume that, it is a portion of left lane line. So, I expand this line according to its slope and then draw that expanded line.
- To get the right lane line, I find the longest line that is located in the right part of the image. I assume that, it is a portion of right lane line. So, I expand this line according to its slope and then draw that expanded line.

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
