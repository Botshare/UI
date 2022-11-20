

## Nodes

**button_handler.py** - Data processing of buttons, reaction of the robot system to pressing buttons on the UI (launching launch files, etc.)

**follow.py** - Saving the route, saving waypoints to a file, deleting waypoints from file, sending waypoints on request from file to topic .

**index.js** - The main file for processing a web page, processing buttons, displaying information, reading and setting velocity.

nav2d.js - The file where the room map is processed, the route points on the map are set, the current position of the robot is displayed on the map.


## Topics

### To package:

**/cmd_vel - geometry_msgs/Twist** - topic for setting the velocity of a robot.

**/raw_vel - geometry_msgs/Twist** - in this topic displays real velocity of a robot

**/map - nav_msgs/OccupancyGrid** -  topic with actual map of the room, data from lidar sensor.

**/robot_pose - geometry_msgs/Pose** - this topic contains a position of a robot on the map coordinate system


### Inside package:

**/may_set_point - std_msgs/Bool** - topic for allow setting the waypoints on the map/

**/new_way_point - geometry_msgs/PoseWithCovarianceStamped** - new waypoint position 

**/WP_req - std_msgs/Empty** - empty request for all saved waypoints

**/WPs_topic - geometry_msgs/PoseArray** - all saved waypoints

**/ui_message - std_msgs/String** - topic for info and exchange information msg

**/ui_operation - std_msgs/String** - topic with command for robot
