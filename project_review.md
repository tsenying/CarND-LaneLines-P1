# Finding Lane Lines on the Road
A part of the Self Driving Car Engineer Nanodegree Program

 
**Meets Specifications**

Hi there!

Congrats on taking the first step towards the Self Driving Car Nano-degree. I hope you enjoyed working on the project. You have done an awesome job implementing the annotations. I have provided some comments and links which you may check out for further improvement.

All the best for your next project :smile:

PS: If you have not already joined the slack community, please do so by going here

## Lane Finding Pipeline

*The output video is an annotated version of the input video.*

Well done providing an annotated output video!

*In a rough sense, the left and right lane lines are accurately annotated throughout almost all of the video. Annotations can be segmented or solid lines*

Fantastic job here. Your left and right lane lines were accurately annotated throughout almost all of the video, as required. You may consider my comments below to further improve the algorithm.

### Suggestions

* increase threshold for Hough Transform - it will increase number of intersections needed to detect a line and as a result reduce number of noise and incorrectly defined lines.
* increase `min_line_len` and `max_line_gap` for Hough Transform to make your lines longer with less number of breaks.

*Visually, the left and right lane lines are accurately annotated by solid lines throughout most of the video.*

The annotated lines are solid for both the left as well as the right lanes. Good!

## Reflection

*Reflection describes the current pipeline, identifies its potential shortcomings and suggests possible improvements. There is no minimum length. Writing in English is preferred but you may use any language.*

Excellent insights have been pointed out and you are on the right path. You have correctly pointed out the need to detect curved lanes.

This [research paper](http://airccj.org/CSCP/vol5/csit53211.pdf) goes into how to detect curves and will also help in detecting faded lanes. It uses an extended version of hough lines algorithm to detect tangents to the curve which can help you detect the curve.

I encourage you to tune your pipeline to implement a better algorithm. You can for example try to implement algorithm provided in this question:
http://stackoverflow.com/questions/36598897/python-and-opencv-improving-my-lane-detection-algorithm
