
## IIWA Teleop Instruction Table(Keyboard)
The table below is the instruction for teleoperating KUKA IIWA robot by using **keyboard** under ROS, which is implemented by running the cmd in terminal:

`rosrun iiwa_teleop_control iiwa_teleop_key`

Generally, there are 4 control modes you can choose:
* JointPosition control
* JointVelocity control
* CartesianPosition control 
* CartesianVelocity control

After running the package, the **default state** is: **JointPosition mode with controlling jointA1 and speedoverride=1.0**.
### JointPosition Mode<a name="JP"></a>

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w / W      |  move in increasing direction | default step size is 10 degree |
| s / S      | move in decreasing direction  |   default step size is 10 degree |
| 1  | select  jointA1 | 
| 2  | select jointA2 | 
| 3  | select jointA3 | 
| 4  | select jointA4 | 
| 5  | select jointA5 | 
| 6  | select jointA6 | 
| 7  | select jointA7 | 
| ' + ' | stepsize + 1 degree | you can modify stepsize and stepstepsize as you want in Config.h file
| ' - ' | stepsize - 1 degree | you can modify stepsize and stepstepsize as you want in Config.h file
| o / O | open gripper | 
| l / L  | close gripper | 
| J | Reset to the **default state**|
| C | switch to the [CatesianPosition Mode](#CP) |
| V | switch to [JointVelocity Mode](#JV)|


### CatesianPosition Mode <a name="CP"></a>

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w / W      |  move forward(x-axis positive) | default step size is 1.7cm |
| s / S      | move backward(x-axis negative)  |   default step size is 1.7cm |
| a / A      | move left(y-axis positive)  |   default step size is 1.7cm |
| d / D      | move right(y-axis negative)  |   default step size is 1.7cm |
| q / Q      | move up(z-axis positive)  |   default step size is 1.7cm |
| e / E      | move down(z-axis negative)  |   default step size is 1.7cm |
|   | select  axis-x | 
| 2  | select axis-y | 

| ' + ' | stepsize + 1 degree | you can modify stepsize and stepstepsize as you want in Config.h file
| ' - ' | stepsize - 1 degree | you can modify stepsize and stepstepsize as you want in Config.h file
| o/O | open gripper | 
| l/L  | close gripper | 
| J | Reset to the **default state**|
| V | switch to **jointVelocity mode**|


### JointVelocity Mode <a name="JV"></a>
