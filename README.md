# homework-4-javtges
## Turtlebot SLAM
### James Avtges


This homework assignemnt involves experimenting with a 2D SLAM package called `slam-toolbox`. The end product is a turtlebot in Gazebo that explores and maps its surroundings.

The launchfiles in this package include:

- `start_slam.launch` : This launchfile allows the user to control a turtlebot using the W, A, S, D, X keys to explore around a house in gazebo and rviz.
- `nav_stack.launch` : This launchfile loads an existing map of the house (made using `start_slam.launch`) and allows the user to give the robot 2D pose goals and have the turtlebot navigate towards them.
- `slam_stack.launch` : This launchfile is similar to `start_slam.launch`, but also starts the `explore` node to automatically explore the house and produce the map.

The node written for this assignment is the `explore` node. It subscribes to the local costmap and the robot's odometry, to obtain its position and its information about the immediate surroundings. It randomly moves around the house by choosing random coordinates within the costmap that are marked as open space.

#### Media


- Testing `nav_stack.launch`
[Testing ](https://www.youtube.com/watch?v=1RVTJSY-gHs&ab_channel=James)

- Testing `slam_stack.launch` with manual movement
[PX100 Arm Gazebo Simulation](https://youtu.be/Weg_5HM9_M4)

- Testing `slam_stack.launch` with automatic movement
[PX100 Arm Real World Test](https://youtu.be/2_Pk6dL4WFc)
