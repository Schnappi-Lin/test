
## IIWA Teleop Instruction Table(Keyboard)
The table below is the instruction for teleoperating KUKA IIWA robot by using **keyboard** under ROS, which is implemented by running the cmd in terminal:

`rosrun iiwa_teleop_control iiwa_teleop_key`

Generally, there are 4 control modes you can choose:
* JointPosition control
* JointVelocity control
* CartesianPosition control 
* CartesianVelocity control

The **Default Mode** is: **JointPosition Mode** with controlling **joint A1** and speedoverride=**1.0**.
### JointPosition Mode<a name="JP"></a>

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w / W      |  move in increasing direction | default step size is 10 degree |
| s / S      | move in decreasing direction  |   default step size is 10 degree |
| 1  | select jointA1 | /
| 2  | select jointA2 | /
| 3  | select jointA3 | /
| 4  | select jointA4 | /
| 5  | select jointA5 | /
| 6  | select jointA6 | /
| 7  | select jointA7 | /
| ' + ' | stepsize + 1 degree | you can modify default_stepsize and stepstepsize as you want in Config.h file
| ' - ' | stepsize - 1 degree | you can modify default_stepsize and stepstepsize as you want in Config.h file
| o / O | open gripper | /
| l / L | close gripper| /
| J | Reset to the **Default Mode**|/
| C | switch to the [CatesianPosition Mode](#CP) |/
| V | switch to [JointVelocity Mode](#JV)|


### CatesianPosition Mode <a name="CP"></a>

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w / W      |  move forward(x-axis positive) | default step size is 0.068m |
| s / S      | move backward(x-axis negative)  |   default step size is 0.068m |
| a / A      | move left(y-axis positive)  |   default step size is 0.068m |
| d / D      | move right(y-axis negative)  |   default step size is 0.068m |
| q / Q      | move up(z-axis positive)  |   default step size is 0.068m |
| e / E      | move down(z-axis negative)  |   default step size is 0.068m |
| r / R      | Roll positive  |   default step size is 3.89 degree |
| f / F      | Roll negative  |   default step size is 3.89 degree |
| t / T      | Pitch positive  |   default step size is 3.89 degree |
| g / G      | Pitch negative  |   default step size is 3.89 degree |
| y / Y      | Yaw positive  |   default step size is 3.89 degree |
| h / H      | Yaw negative  |   default step size is 3.89 degree |
| ' + ' | stepsize + 1cm in linear or -1 degree in orient | you can modify default stepsize and stepstepsize in Config.h file
| ' - ' | stepsize - 1cm in linear or -1 degree in orient | you can modify default stepsize and stepstepsize in Config.h file
| o/O | open gripper | /
| l/L  | close gripper | /
| J | switch to [JointPosition Mode](#JP)|/
| V | switch to [CartesianVelocity Mode](#CV)|/

### JointVelocity Mode <a name="JV"></a>
For safty reason, the speedoverride will be automatically set to 0.5 when enter to this mode,and the initial joint velocity=0 rad/s

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| continue press w / W      |  move in increasing direction | notice that default velocity is 0
| continue press s / S      |  move in decreasing direction | notice that default velocity is 0
| 1  | select jointA1 | the velocity reset to 0 
| 2  | select jointA2 | the velocity reset to 0 
| 3  | select jointA3 | the velocity reset to 0 
| 4  | select jointA4 | the velocity reset to 0 
| 5  | select jointA5 | the velocity reset to 0 
| 6  | select jointA6 | the velocity reset to 0 
| 7  | select jointA7 | the velocity reset to 0 
| ' + ' | velocty + 0.1 rad/s | you can modify velocity_step_size(0.1 rad/s) as you want in Config.h file
| ' - ' | velocity - 0.1 rad/s | you can modify velocity_step_size(0.1 rad/s) as you want in Config.h file
| o / O | open gripper | /
| l / L | close gripper| /
| J | Reset to the **default state**|/
| C | switch to the [CatesianPosition Mode](#CP) |/
| V | switch to [JointVelocity Mode](#JV)|

### TODO:CartesianVelocity Mode <a name="CV"></a>
| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w / W      |  move forward(x-axis positive) | default step size is 0.068m |
| s / S      | move backward(x-axis negative)  |   default step size is 0.068m |
| a / A      | move left(y-axis positive)  |   default step size is 0.068m |
| d / D      | move right(y-axis negative)  |   default step size is 0.068m |
| q / Q      | move up(z-axis positive)  |   default step size is 0.068m |
| e / E      | move down(z-axis negative)  |   default step size is 0.068m |
| r / R      | Roll positive  |   default step size is 3.89 degree |
| f / F      | Roll negative  |   default step size is 3.89 degree |
| t / T      | Pitch positive  |   default step size is 3.89 degree |
| g / G      | Pitch negative  |   default step size is 3.89 degree |
| y / Y      | Yaw positive  |   default step size is 3.89 degree |
| h / H      | Yaw negative  |   default step size is 3.89 degree |
| ' + ' | stepsize + 1cm in linear or -1 degree in orient | you can modify default stepsize and stepstepsize in Config.h file
| ' - ' | stepsize - 1cm in linear or -1 degree in orient | you can modify stepsize and stepstepsize in Config.h file
| o/O | open gripper | /
| l/L  | close gripper | /
| J | switch to the [JointPosition Mode](#JP)|/
| V | switch to [CartesianVelocity Mode](#CV)|/
