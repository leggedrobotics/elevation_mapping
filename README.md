Robot-Centric Elevation Mapping
======================

**WARNING: Writing of this document is still under progress!** 

Overview
---------------

This is a collection of [ROS] packages developed for local elevation mapping with a mobile robot. The software is designed for (local) navigation tasks with robots which are equipped with a pose estimation (e.g. IMU & odometry) and a distance sensor (e.g. kinect, laser range sensor). The provided elevation map is limited around the robot and reflects the pose uncertainty that is aggregated through the motion of the robot (robot-centric mapping). This method is developed to explicitly handle drift of the robot pose estimation.

The Robot-Centric Elevation Mapping packages have been tested under ROS-Groovy and Ubuntu 13.04. This is research code, expect that it changes often and any fitness for a particular purpose is disclaimed.

**Author: Peter Fankhauser, pfankhauser@ethz.ch<br />
Affiliation: Autonomous Systems Lab, ETH Zurich**

Citing
---------------

The robot-centric elevation mapping methods used in this software are described in the following paper (available [here]()).

P. Fankhauser, M. Bloesch, C. Gehring, M. Hutter, and R. Siegwart,
**"Robot-centric elevation mapping with uncertainty estimates"**,
in Climbing and Walking Robots (CLAWAR), 2014.

    @inproceedings{Fankhauser2014RobotCentricElevationMapping,
      author = {Fankhauser, Péter and Bloesch, Michael and Gehring, Christian and Hutter, Marco and Siegwart, Roland},
      title = {Robot-centric elevation mapping with uncertainty estimates},
      booktitle = {Climbing and Walking Robots (CLAWAR)},
      year = {2014}
    }

Watch the [video](http://www.youtube.com/watch?v=I9eP8GrMyNQ) demonstrating the Robot-Centric Elevation Mapper: 
[![Robot-Centric Elevation Mapping](example.jpg)](http://www.youtube.com/watch?v=I9eP8GrMyNQ)

Installation
------------

### Dependencies

This software is built on the Robotic Operating System ([ROS]), which needs to be [installed](http://wiki.ros.org) first.

Additionaly, the Robot-Centric Elevation Mapper depends on following software:

- [Eigen](http://eigen.tuxfamily.org) linear algebra library,

### Building

In order to install the Robot-Centric Elevation Mapper, clone the latest version from this repository into your catkin workspace and compile the package using ROS.

    cd catkin_workspace/src
    git clone https://github.com/ethz-asl/elevation_mapping.git
    cd ../
    catkin_make

### Running the Unit Tests

Bugs
------------

Please report bugs and request features using the [Issue Tracker](https://github.com/ethz-asl/elevation_mapping/issues).

[ROS]: http://www.ros.org

