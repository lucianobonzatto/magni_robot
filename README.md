
# Overview

This package contains launch files and configuration files for the Magni robot.

# Installation
https://learn.ubiquityrobotics.com/simulation

## Launch files

### magni_demos fiducial_follow.launch

Runs everything for the fiducial follow demo. 

### magni_demos simple_navigation.launch

Runs a simple fiducial based navigation demo using fiducials and move_basic. The robot is controllable using Robot Commander.

### magni_nav aruco.launch

This launch file runs the fiducial marker based localization system using Raspberry Pi camera, configured to run on Magni.
For more information, see [fiducials](http://wiki.ros.org/fiducials) and
[raspicam_node](https://github.com/UbiquityRobotics/raspicam_node)

### magni_nav move_basic.launch

This launch file runs the [move_basic](https://github.com/UbiquityRobotics/move_basic) simple navigation system with the parameters needed for Magni.

### magni_viz view_nav.launch

To be run on a workstation, not the pi. This brings up rviz in a way suitable to visualize fiducial based navigation. 

### magni_viz view_robot.launch

To be run on a workstation, not the pi. This brings up rviz in a way suitable to visualize just the state of the robot and sensors, without a navigation stack.

## Internal

### magni_bringup base.launch

Runs everything needed for teleop, including Robot Commander based teleop (no navigation). Runs on robot boot. To see the full detailed documented boot procedure see [magni_bringup README](magni_bringup/README.md)

### magni_description description.launch
Internal launch file for making the URDF load and robot_state_publisher work.

You should not have to run this launch file directly.

## Software that enables core hardware functionality on Magni:

    https://github.com/UbiquityRobotics/ubiquity_motor     - Makes the Motors work; Package; no UI; no documentation

    https://github.com/UbiquityRobotics/raspicam_node      - Makes the Cameras work; Package; Calibration UI (documented)--is this exposed to User? 

    Motor controller firmware -- not to be released.
