# **Finding Lane Lines on the Road**

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:

* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

[//]: # (Image References)

[image1]: ./test_images_output/gray_solidWhiteCurve.jpg "Grayscale"

[image2]: ./test_images_output/blur_solidWhiteCurve.jpg "Blur"

[image3]: ./test_images_output/edge_solidWhiteCurve.jpg "Edge"

[image4]: ./test_images_output/msk_edge_solidWhiteCurve.jpg "Masked Edge"

[image5]: ./test_images_output/line_solidWhiteCurve.jpg "Line"

[image6]: ./test_images_output/solidWhiteCurve.jpg "Annotated"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.

#### Step 1. Converted to grayscale

I did this to work with only brightness values

![alt text][image1]

#### Step 2. Blurred image using Gaussian Filter

Used gaussian filter to get rid of noise

![alt text][image2]

#### Step 3. Found edges of image using Canny Edge Detector

![alt text][image3]

#### Step 4. Masked region of interest with coordinates of road

Other edges are not informative right now to decide lane we are driving
![alt text][image4]

#### Step 5. Using hough transform found lines and draw them according to slopes

In order to decide lines and draw them, I extracted slope(m) and bias(b) from every line. Then, filtered slope to
operate in a reasonable range of values. After filtering, I classified them as right and left values by using signature
of slopes. I averaged filtered and classified values. Using average m and b values, I calculated x1, x2, y1 and y2 for
left and right lanes

![alt text][image5]

#### Step 6. Placed lines into image.

![alt text][image6]

### 2. Identify potential shortcomings with your current pipeline

One shortcoming is that this algorithm can not fit into curvy lanes. Another one is about slope of lanes. This algorithm
decides side of lane line by sign of slope value. However, both lanes can be trending towards same sides and have same
sign for left and right. This is not covered for lane finding pipeline

### 3. Suggest possible improvements to your pipeline

For curvy lanes, smapling lines and using curve fitting can be done. For slope problem, bias of lanes can be explored to
get a midpoint to classify left and right.
