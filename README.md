# Robot---SLAM

Thanks to the Occupancy Grid Mapping algorithm, with this project it is possible to map the surfaces of the environment in which the robot is placed. Continuous Bag of Words model is used to determine the important features of the images obtained using a depth camera. With the rtabmapping package the robot can build the map of its environment. 
Going around, the algorithm builds the map based on the loop closures. The robot is moved through turtle bot teleop twist keyboard.

## Execution
- Init your catkin_ws
- Go to the catckin workspace and clone this repository.
- `catkin_make`

## Open terminal 1
```
source devel/setup.bash
roslaunch my_robot world.launch
```

## Open terminal 2
```
source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

## Open terminal 3
```
roslaunch my_robot mapping.launch
```

You can now drive the robot with the keyboard around, to map the environment.

## Open terminal 4 (To vew the db file after 3 loops)
```
rtabmap-databaseViewer ~/.ros/rtabmap.db
```
