### `1.2 编写ROS节点` 中 记录下来的一些命令

```
$ mkdir -p ros_ws/src
# cd ros_ws/src
$ catkin_create_pkg my_minimal_nodes roscpp std_msgs
# add cpp to my_minimal_nodes/src
# update CMakeLists.txt
# cd ros_ws dir
$ catkin_make
$ source devel/setup.bash
# tty1
$ roscore
# tty2
$ rosrun my_minimal_nodes my_minimal_publisher
# tty3
$ rosrun my_minimal_nodes my_minimal_subscriber
```

