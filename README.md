# Roomba Robot
[![Build Status](https://travis-ci.org/urastogi885/roomba-robot.svg?branch=master)](https://travis-ci.org/urastogi885/roomba-robot)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

## Overview

ROS package to simulate multiple behaviors on a robot

## Dependencies

- Ubuntu 16.04
- ROS Kinetic
- Gazebo

## Install Dependencies

- This project was developed using ROS Kinetic.
- It is highly recommended that ROS Kinetic is properly installed on your system before the use of this project.
- Follow the instructions on this [*link*](http://wiki.ros.org/kinetic/Installation/Ubuntu) to install ***Full-Desktop 
  Version*** of ROS Kinetic.
- The full-version would help you install *Gazebo* as well. If you have ROS Kinetic pre-installed on your machine, use
  the following [*link*](http://gazebosim.org/tutorials?tut=install_ubuntu&cat=install) to install *Gazebo* on your
  machine.
- Ensure successful installation by running *Gazebo* via your terminal window:
```shell script
gazebo
```
- A window of *Gazebo Simulator* should be launched.
- Create your ROS workspace by following instructions on this [*link*](http://wiki.ros.org/catkin/Tutorials/create_a_workspace).

## Build

- Switch to your *src* sub-directory of your ROS workspace to clone this repository.
```shell script
<ROS Workspace>/src
```
- Run the following commands to clone and build this project:
```shell script
git clone --recursive https://github.com/urastogi885/obstacle_avoidance_simulation
cd robo_behaviors/
chmod +x reading_laser.py
chmod +x obstacle_avoidance.py
chmod +x wall_following.py
cd ../../
catkin_make
```

## Run

- In the same terminal, run:
```shell script
roscore
```
- Open a new terminal, switch to the ROS workspace, and launch the manual mode:
```shell script
cd <ROS Workspace>
source devel/setup.bash
roslaunch my_first_robot manual_mode.launch
```
- A 2-wheeled bot will open up on the Gazebo Simulator and you will be able to control the robot with standard teleop
commands.
- Change your camera view to have better look at the movement of the robot.
- Stop execution using *Ctrl+C*.
- Open a new terminal, switch to the ROS workspace, and launch the obstacle avoidance node:
```shell script
cd <ROS Workspace>
source devel/setup.bash
roslaunch my_first_robot follow_wall.launch
```
- The robot will display obstacle avoidance along with wall-following behavior.
- Change your camera view to have better look at the movement of the robot.
- Stop execution using *Ctrl+C*.
