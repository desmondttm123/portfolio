---
layout: default
title: "Robocup"
---

<style>
  /* Custom styles for the select dropdown */
  nav {
    margin: 20px;
  }

  .menu-select {
    appearance: none; /* Remove default styling */
    -webkit-appearance: none; /* Remove default styling for WebKit browsers */
    -moz-appearance: none; /* Remove default styling for Firefox */
    background-color: #fff;
    border: 1px solid #ccc;
    padding: 10px;
    font-size: 16px;
    border-radius: 5px;
    width: 50%;
    max-width: 50%; /* Ensure the dropdown takes full width on mobile */
    margin-bottom: 10px; /* Space between dropdowns */
    cursor: pointer;
    transition: background-color 0.3s, border-color 0.3s;
  }

  .menu-select:hover {
    background-color: #f0f0f0;
    border-color: #bbb;
  }

  .menu-select:focus {
    outline: none;
    border-color: #007BFF;
  }

  .menu-select option {
    background-color: #fff;
    color: #000;
  }

  /* Custom dropdown arrow */
  .menu-select {
    background-image: url('data:image/svg+xml;charset=US-ASCII,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 4 5"><path fill="%23000" d="M2 0L0 2h4z"/></svg>');
    background-repeat: no-repeat;
    background-position: right 10px center;
    background-size: 8px 10px;
    padding-right: 30px; /* Add space for the arrow */
  }

  /* Ensure select dropdown looks good on mobile */
  @media (max-width: 768px) {
    nav {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .menu-select {
      max-width: 90%; /* Ensure dropdown takes most of the screen width */
    }
  }
</style>

<nav>
  <select class="menu-select" onchange="location = this.value;">
    <option value="">☰ Tasks</option>
    <option value="{{ site.baseurl }}/">Home</option>
    <option value="{{ site.baseurl }}/robocup">Robocup</option>
    <option value="{{ site.baseurl }}/projects">Projects</option>
    <option value="{{ site.baseurl }}/contact">Contact</option>
    <option value="{{ site.baseurl }}/about">About</option>
  </select>
</nav>

# Mainrobot Simulation
This is a launch file for the humanoid robot in gazebo.

### Launch the robot in gazebo
```py
ros2 launch mainrobot_description launch_sim.launch.py
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/mainrobot_description/config/mapper_params_online_async.yaml use_sim_time:=true
```