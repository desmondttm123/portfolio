---
layout: default
title: "Robocup"
---

# Mainrobot Simulation
This is a launch file for the humanoid robot in gazebo.

### Launch the robot in gazebo
```py
ros2 launch mainrobot_description launch_sim.launch.py
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/mainrobot_description/config/mapper_params_online_async.yaml use_sim_time:=true
```

# Moveit2 Launch File
This is a launch file for the humanoid robot arm in gazebo.

### Launch the RVIZ2 Preview
```py
ros2 launch mainrobot_moveit_config_humble mainrobot_moveit.launch.py
```
