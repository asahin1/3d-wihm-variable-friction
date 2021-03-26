# wihm-variable-friction
This folder currently contains the low and high level command nodes for the variable friction hand, the manipulation environment, and simulation plugin for variable friction mechanism.

## Packages:

### gripper_controls
This package is based on the motion planning nodes in variable_friction_gripper project, which were prepared to be used on hardware. Same logic and functionality is transferred to the gazebo simulation in this package.

Low level controller is based on the class LowLvlController and deals with low level tasks such as receiving and publishing effort, position references, friction values for the left and right fingers.

High level controller is based on the class Hand. It advertises services of high level commands such as, Hold_object, Slide_Left_Finger_Down, Slide_Left_Finger_Up, Slide_Right_Finger_Down, Slide_Right_Finger_Up, Rotate_clockwise, Rotate_anticlockwise, by using the low level commands.

Also a sequential command node is included, that helps testing the services advertised by the high level controller. It is possible to use the torque publisher and a plotting method of your own choice to analyse the gripper behavior during tasks.

high_lvl_ctrl and low_lvl_ctrl nodes can either be run seperately, or you may use the launch file that launches both controllers.
> This package contains:
> 1. yaml config files for low level and high level controller parameters
> 2. launch file for gripper controller
> 3. Implementation of high and low level controllers
> 4. A sequential command node for testing the advertised services
> 4. A torque publisher for analysing the gripper behavior
> 5. Readme file for available services

### manipulation_env
This package is used to generate a manipulation environment. Manipulation environment currently consists of a table and a rectangular block object. Collision characteristics of the block object plays an important role in the manipulation performance. Parameters such as friction coefficients, Kp and Kd can be modified within the corresponding description file.
> This package contains:
> 1. description files for objects
> 2. launch file for launching the integrated arm & gripper in a manipulation environment
> 3. launch file for gripper only (for testing purposes) in a manipulation environment

### simulation_plugings
> This package contains a gazebo plugin for varying friction in runtime.
