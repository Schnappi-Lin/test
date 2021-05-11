
## IIWA Teleop Instruction Table(Keyboard)
The table below is the instruction for teleoperating KUKA IIWA robot by using **keyboard** under ROS, which is implemented by running the cmd in terminal:

`rosrun iiwa_teleop_control iiwa_teleop_key`

Generally, there are 4 control modes you can choose:
* JointPosition control
* JointVelocity control
* CartesianPosition control 
* CartesianVelocity control

After running the package, the default state is: **JointPosition mode with controlling jointA1 and speedoverride=1.0**.
### JointPosition Mode

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| w/W      |  move in increasing direction | default step size is 10 degree |
| s/S      | move in decreasing direction  |   default step size is 10 degree |
| 1  | select  jointA1 | 
| 2  | select jointA2 | 
| 3  | select jointA3 | 
| 4  | select jointA4 | 
| 5  | select jointA5 | 
| 6  | select jointA6 | 
| 7  | select jointA7 | 
| Shift + '+' | stepsize + 1 degree | you can modify stepsize and stepstepsize as you want in Config.h file
| V | switch to **jointVelocity mode**|


