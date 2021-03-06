# Trajectory_generation_based_on_Monocular_Visual_Odometry
Our team developed a monocular visual odometry app to generate a trajectory for the user’s movement in real time. The application is implemented with the support of OpenCV library. When the app is on, it could draw a trajectory in real time for the user who walks in an environment with enough feature. The limits of capacity of CPU in mobile phones make it a challenging problem.
# Introduction
Visual Odometry is the estimation of 6-DOF trajectory followed by a moving agent, based on input from a camera rigidly attached to the body of the agent [1]. It has attracted a lot of research in the recent years, it was originally intended to be used on Mars Rover, where there is no GPS and wheel odometry becomes unreliable due to slip on the sandy martian surface [2]. In recent years, visual odometry has also found uses in autonomous driving, wearable electronics, augmented reality, and even gaming. In space exploration and robot task planning problem, the environment is often partly unknown. Thus using visual odometry to generate trajectory is very useful in this kind of research. 
We use FAST corner detector for feature detection and KLT algorithm for feature tracking. We use five-point algorithm to compute the essential matrix and then compute rotation matrix and transition vector from E to construct the trajectory.
Nowadays, mobile phone is extremely common in our daily life. Implementation of Visual Odometry on mobile platforms could be used to navigate blind person in indoor and outdoor environment. A visual odometry placed into a vision app could is also very portable, since a mobile phone can be attached to a robot easily.
# Background
I write our code based on Avi Singh’s Github project Monocular Visual Odometry using OpenCV, which only works on image dataset with groundtruth. 
# Results
In this section, we make the app run under straightway, curve, back and forth, U-turn and loop circumstances. Actually, to get a relatively good performance, we have to move relative slow when take turns in case that the feature tracking fails and triggering redetection too often. Moreover, if the surroundings have too few features to below a preset threshold (500 here), it won’t work.
# Notificaiton
You need to download the opencv.framework by yourself to make this project work on your own devices.
