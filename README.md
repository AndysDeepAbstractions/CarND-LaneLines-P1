
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
  + i modified this for the Challange Video 
- added a little gaussian_blur
- applyed canny
- masked the image
- applyed hough_lines (multiple times with diffrent parameters)

In order to draw a single line on the left and right lanes, i added multiple hough transform layers and adjusted the parameters till the test images look fine. This is done to build a model that dont craches hard on lane change.

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
- Continous lines should be treathed diffrtent then dashed ones
- Optical corrections shoud be applyed
- Frame overlapping processing

Another potential improvement could be to use stereo vision