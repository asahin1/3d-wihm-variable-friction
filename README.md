# Within-Hand-Manipulation using Variable Friction Fingers
This repository includes the simulation environment and command nodes for within hand manipulation using variable friction fingers.

To start using:
1. Source the workspace.

2. Launch the manipulation environment in gazebo.
```
  roslaunch manipulation_env vf_only.launch
```
3. Unpause the simulation.

4. Use rosservices to command the varible friction hand (details are provided within [vf_hand_sim/gripper_controls](https://github.com/asahin1/wihm-variable-friction/tree/main/vf_hand_sim/gripper_controls).

5. The object shape and the configuration of the manipulation environment can be modified through the description files within [vf_hand_sim/manipulation_env/desc](https://github.com/asahin1/wihm-variable-friction/tree/main/vf_hand_sim/manipulation_env/desc) and the launch file within [vf_hand_sim/manipulation_env/launch](https://github.com/asahin1/wihm-variable-friction/tree/main/vf_hand_sim/manipulation_env/launch).
