# Robotic Software Engineer ND 
## Project 4: Map My World

[image1]: ./img/RobotND-Project4-Gazebo-World.png  " "
[image2]: ./img/RobotND-Project4-RVIZ.png " "
[image3]: ./img/RobotND-Project4-RTAB-Map-database.png " "


Simple ROS/Gazebo project for Mapping with RTAB-Map package using an RGBD camera and a laser range finder.

Gazebo world with mobile robot:
![][image1]

Rviz with partial map from RTAM-Map:
![][image2]

RTAM-Map database viewer with complete map:
![][image3]

## How To Use

### Clone repo as catkin_ws, initialize workspace and build
```
$ git clone https://github.com/civcode/RobotND-P4-MapMyWorld.git catkin_ws
$ cd catkin_ws/src 
$ catkin_init_workspace
$ cd .. && catkin_make
```

### Launch ROS and Gazebo
```
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```

### Launch RTAB-Map Mapping
```
$ source devel/setup.bash
$ roslaunch my_robot mapping.launch
```

### View the complete Map
Download the map <a href="https://drive.google.com/file/d/1yMyZXRvi69aKtDSvoKm97CBK0_UrLJxa/view?usp=sharing" target="_blank">rtabmap-final.db</a> (163 MB).
```
$ rtabmap-databaseViewer rtabmap-final.db
```

