
## IIWA Teleop Instruction Table(Keyboard)
The table below is the instruction for teleoperating KUKA IIWA robot by using **keyboard** under ROS, which is implemented by running the cmd in terminal:

`rosrun iiwa_teleop_control iiwa_teleop_key`

Generally, there are 4 control modes you can choose:(TODO: add a state machine picture here)
* JointPosition control
* JointVelocity control
* CartesianPosition control 
* CartesianVelocity control

The **Default Mode** is: [JointPosition Mode](#jp). 

### <a name="jp"></a>  JointPosition Mode
For each time enter into this mode: control object reset to **joint A1** , step size reset to **default step size**, speedoverride will reset to **1.0**.

| Command        |     Description      |Remark   |
| :-------------: |:-------------:| :-----:|
| `w / W`      |  move in increasing direction | default step size is 10° |
| `s / S `     | move in decreasing direction  |   default step size is 10° |
| `1`  | select jointA1 | /
| `2`  | select jointA2 | /
| `3`  | select jointA3 | /
|` 4`  | select jointA4 | /
| `5`  | select jointA5 | /
| `6`  | select jointA6 | /
|` 7`  | select jointA7 | /
| ` + ` | stepsize + 1 degree | you can modify default_stepsize and stepstepsize in Config.h file
| ` - ` | stepsize - 1 degree | you can modify default_stepsize and stepstepsize in Config.h file
| `p / P` | print current joint angles and cartesian pose| /
| `o / O` | open gripper | /
| `l / L` | close gripper| /
| `J` | switch to [JointPosition Mode](#jp)|/
|` C` | switch to [CatesianPosition Mode](#cp) |/
| `V` | switch to [JointVelocity Mode](#jv)|


### CatesianPosition Mode <a name="cp"></a>
For each time enter into this mode: step size will reset to **default step size**, speedoverride will reset to **1.0**.

| Command        |     Description      |Remark   |
|:-------------:|:-------------:| :-----:|
| `w / W`      |  move forward(x-axis positive) | default step size is 0.068m |
| `s / S`      | move backward(x-axis negative)  |   default step size is 0.068m |
| `a / A`      | move left(y-axis positive)  |   default step size is 0.068m |
| `d / D`     | move right(y-axis negative)  |   default step size is 0.068m |
| `q / Q`      | move up(z-axis positive)  |   default step size is 0.068m |
| `e / E`      | move down(z-axis negative)  |   default step size is 0.068m |
| `r / R`      | Roll positive  |   default step size is 3.89° |
| `f / F`      | Roll negative  |   default step size is 3.89° |
| `t / T`      | Pitch positive  |   default step size is 3.89°|
| `g / G`      | Pitch negative  |   default step size is 3.89° |
| `y / Y`      | Yaw positive  |   default step size is 3.89° |
| `h / H`      | Yaw negative  |   default step size is 3.89° |
| ` + `| stepsize + 1.7cm in linear or +1 degree in orient | you can modify default stepsize and stepstepsize in Config.h file
| ` - ` | stepsize - 1.7cm in linear or -1 degree in orient | you can modify default stepsize and stepstepsize in Config.h file
| `p / P` | print current joint angles and cartesian pose| /
| `o / O` | open gripper | /
| `l / L`  | close gripper | /
| `J` | switch to [JointPosition Mode](#jp)|/
| `C` | switch to the [CatesianPosition Mode](#cp) |/
| `V` | switch to [CartesianVelocity Mode](#cv)|/

### JointVelocity Mode <a name="jv"></a>
For safty reason, the speedoverride will be automatically set to 0.5 when enter to this mode,and the initial joint velocity=0 rad/s

| Command        |     Description      |Remark   |
| ------------- |:-------------:| :-----:|
| continue press` w / W`      |  move in increasing direction | notice that default velocity is 0
| continue press` s / S`      |  move in decreasing direction | notice that default velocity is 0
|` 1`  | select jointA1 | the velocity will reset to 0 
| `2 ` | select jointA2 | the velocity will reset to 0 
| `3`  | select jointA3 | the velocity will reset to 0 
|` 4 ` | select jointA4 | the velocity will reset to 0 
|` 5`  | select jointA5 | the velocity will reset to 0 
| `6 ` | select jointA6 | the velocity will reset to 0 
| `7`  | select jointA7 | the velocity reset to 0 
| ` + ` | velocty + 0.1 rad/s | you can modify velocity_step_size(0.1 rad/s) as you want in Config.h file
| ` - ` | velocity - 0.1 rad/s | you can modify velocity_step_size(0.1 rad/s) as you want in Config.h file
|` o / O` | open gripper | /
| `l / L` | close gripper| /
| `J` | switch to [JointPosition Mode](#jp)|/
| `C` | switch to [CatesianPosition Mode](#cp) |/
| `V` | nothing change|

### TODO:CartesianVelocity Mode <a name="cv"></a>
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
| `J` | switch to [JointPosition Mode](#jp)|/
| `C` | switch to [CatesianPosition Mode](#cp) |/
| `V` | nothing change|
