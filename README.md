# Aim
This algorithm overlays a line of specified length(in cm) on an image. The length of line, slope and starting point are provided by the user through a GUI.

# Motivation
This algorithm was developed for [MATE ROV International Competition 2017/18](https://materovcompetition.org/).  The mission was aimed at placing an object at a distance specified by the judges using an underwater robot. Using the judge provided reference object, this algorithm computed the scale and performed some other mathematical calculations to overlay a line of the specified length in the frame of reference of the captured image. This indicated to the pilot driving the robot, the point in the screen, where the object shall be placed.


# Video Demonstration
[Shows how to operate this GUI](https://drive.google.com/file/d/1pp4FO25x33s_C7ZK2XLr7s9EFRRQbNHq/view?usp=sharing)


# Setup/Installation
1. Install python-opencv
2. Install PyQt4
3. Execute 'DistanceMeasurement.py' to run this algorithm on the test image 'test1.png'


# Operation
1. Once the GUI is running, enter the distance of the line you want to overlay on 'test1.png'
2. Provide the direction of this line by entering the starting point and any other point on the line. Do this by clicking on the starting point in the image and then pressing the 'First Point' to store the starting co-ordinates. Then again click on the image and press the'Second Point' to enter the co-ordinates of any other point on this line. Then press 'Slope' button to store the calculated slope. Note: To calculate the direction of a line a minimum of two points are required and hence this process was done
3. Now, provide GUI with the start and end co-ordinates of the object that you know as the reference. Reference objects are those for which you know the exact length. Therefore press the 'First Point' and 'Second Point' as shown in the video. Make sure the points are selected in the correct order. In the attached video the reference used was the vertical length of one of the ends of the calliper of 40cm. 
4.Since this reference length is a known value, you have to change this in the code for your usage. Therefore, modify the 'self.actualDistance' to the length of your reference object. This length is used for calculating the scaling factor.
5. Press 'Result' to draw the required distance on the image


# Testing
Multiple images were captured with the vernier calliper having a different orientation and distance between its two ends. The reference distance was kept the same, and the distance between the ends of the calliper was calculated for these images using this algorithm. A high accuracy was achieved with only +/- 0.01% error between the overlayed and the actual distance.
