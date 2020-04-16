# Autonomous Landing Data Analysis
This project is the data analysis of the results obtained from a simulation of an autonomous landing system of a UAV using ROS and Gazebo. In the [autonomous_landing_uav](https://github.com/MikeS96/autonomous_landing_uav) repository you can find the simulation of the UAV (DJI f450) from which the data was obtained to perform the analysis.

## Requirements
Python3:
 * jupyter-notebook
 * pandas
 * matplotlib
 * seaborn

## Detection Analysis
The [detection analysis](/detection_analysis.ipynb) is the analysis of the errors obtained from the detection process of the landing system to locate the landing platform. This detection process was performed three times using three different detectors: ORB, SIF and SURF. The objective of this analysis was to determine which of the detectors have a better performance.

It was decided that the SIFT detector has a better performance because for each error a graph of vilin plots comparing the three detectors was made and the SIFT detector had a median closer to zero and that the standard deviation was the smaller compared to the other two detectors.

## Controller Errors Analysis
The [detection analysis](/detection_analysis.ipynb) is the analysis of the errors obtained from the autonomous landing process on the platform. Three controllers were tested (P Proportional, PI Proportinal-Integral, PID Proportinal-Integral-Derivative), five times each, to determine which of them have a better performance.
