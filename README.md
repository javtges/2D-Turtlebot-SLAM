# homework-4-javtges
## Turtlebot SLAM
### James Avtges


This homework assignemnt involves experimenting with a 2D SLAM package called `slam-toolbox`. The end product is a turtlebot in Gazebo that explores and maps its surroundings. It uses the package MoveBase to plan the turtlebot's path, AMCL for localization, and online asynchronous mapping provided by the slam toolbox.

The launchfiles in this package include:

- `start_slam.launch` : This launchfile allows the user to control a turtlebot using the W, A, S, D, X keys to explore around a house in gazebo and rviz.
- `nav_stack.launch` : This launchfile loads an existing map of the house (made using `start_slam.launch`) and allows the user to give the robot 2D pose goals and have the turtlebot navigate towards them. It also loads gazebo and the rviz sensor visualization.
- `slam_stack.launch` : This launchfile is similar to `start_slam.launch`, which allows the user explore the house and produce the map. It also loads gazebo and the rviz sensor visualization.
- `auto_slam.launch` : This launchfile includes `slam_stack.launch`, and also launches the `explore` node to automatically explore the house.

The node written for this assignment is the `explore` node. It subscribes to the local costmap and the robot's odometry, to obtain its position and its information about the immediate surroundings. It randomly moves around the house by choosing random coordinates within the costmap that are marked as open space.

#### Media

- Testing `nav_stack.launch` - 4x speed
[Nav Stack](navStack.gif)

- Testing `slam_stack.launch` with manual movement, 4x speed
[Slam Stack](slamStack.gif)

- Testing `slam_stack.launch` with automatic movement, 4x speed
[Auto Slam](autoSlam.gif)
