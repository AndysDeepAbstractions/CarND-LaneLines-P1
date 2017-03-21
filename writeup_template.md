
**Finding Lane Lines on the Road**

The goals / steps of this project are the following:

* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg     "solidWhiteCurve"   
[image2]: ./test_images_output/solidWhiteRight.jpg     "solidWhiteRight"
[image3]: ./test_images_output/solidYellowCurve.jpg    "solidYellowCurve" 
[image4]: ./test_images_output/solidYellowCurve2.jpg   "solidYellowCurve2"  
[image5]: ./test_images_output/solidYellowLeft.jpg     "solidYellowLeft"
[image6]: ./test_images_output/whiteCarLaneSwitch.jpg  "whiteCarLaneSwitch"

---

### Reflection

###1. Pipeline description:

This pipeline consisted of 5-6 steps. 

- Images to grayscale 
- added a little gaussian_blur
- applyed canny
- masked the image
- applyed hough_lines (two times with diffrent parameters)

In order to draw a single line on the left and right lanes, i added a huge maximum gap in pixels between connectable line segments to the second hough transform and atjusted the parameters till the test images look fine.

![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]
![alt text][image5]
![alt text][image6]


###2. Potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when 

- Lanes are not straigt lines
- Weather or light changes


###3. Possible improvements to your pipeline

- Adjust paramethers futher
- Add a nother hughg layer

Another potential improvement could be to use stereo vision