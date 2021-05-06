# IIWA_TELEOP
This project is for teleoperating KUKA IIWA Robot by using **keyboard** or **joystick**, or even your own **body** in ROS.

## Fast application
### Setup for Robot
After turning on the robot, on the KUKA SmartPAD under "**Station**"->"**Process Data**", select "**ROS Master IP**" tag,

If your master laptop IP address is: **10.2.0.55**

then, change value to be the same as **10.2.0.55**

Go to "Applications", select and Run the application: **ROSSmartServo**, the robot will be ready and wait for the master. 

### Using Keyboard
first clone the package to your laptop *catkin_ws* workspace

`cd catkin_ws`

`git clone xxx_iiwa_teleop_control`

`catkin_make`

setup your ROS Master IP (you can run `ip address` to check your laptop's IP, below we use IP = 10.2.1.17 to be as an example):

`export ROS_IP=10.2.1.17`   

`export ROS_MASTER_URI=http://$ROS_IP:11311`

`source .bashrc`

run ros master core:

`roscore`
 
 open a new terminal and run:
 
` rosrun iiwa_teleop_control iiwa_teleop_key`

then you can control the robot by using keyboard accordding to the instructions table.

### Using Joystick
The same as **Using Keyboard** except the last step we run:

`rosrun joy joy_node`
 
`rosrun iiwa_teleop_control iiwa_teleop_joy`

Here is the joystick control instruction table.

### Using Human body


