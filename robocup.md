---
layout: default
title: "Robocup"
---

# Simulation Launch File
This is a launch file for the humanoid robot in gazebo.

```py
ros2 launch mainrobot_description launch_sim.launch.py
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/mainrobot_description/config/mapper_params_online_async.yaml use_sim_time:=true
```
