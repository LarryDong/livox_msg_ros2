
# Compile livox_ros_driver CustomMsg


```bash
mkdir livox_msgs_ws
# then donwload the codes

# build & source
colcon build --symlink-install
source install/setup.bash

# run
ros2 bag play <xxx>
```

## For livox_ros_driver1 or 2
For livox_ros_dirver, modify:  
`CMakeLists.txt`, `package.xml`, livox_ros_driver2 -> livox_ros_driver

For livox_ros_dirver2, modify:  
`CMakeLists.txt`, `package.xml`, livox_ros_driver -> livox_ros_driver2

## For ROS1
ROS1 compile using `catkin`, using `CMakeLists_ROS1.txt` and `package_ROS1.xml`

