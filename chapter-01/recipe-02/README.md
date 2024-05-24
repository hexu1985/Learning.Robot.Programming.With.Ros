### 1.3.1 用catkin_simple简化CmakeLists.txt` 中 记录下来的一些命令

```
# clone catkin_make.git
# git clone git@github.com:catkin/catkin_simple.git
# cd ros_ws/src
# ln catkin_simple to catkin_simple.git dir

# cp cs_create_pkg.py from learning_ros_external_packages/cs_create_pkg.py
# alias cs_create_pkg='path of cs_create_pkg.py'
# example: alias cs_create_pkg='~/git/demo_code/ros/cs_create_pkg.py'

# cd ros_ws/src
$ cs_create_pkg my_minimal_nodes2 roscpp std_msgs

# add cpp to my_minimal_nodes2/src
# update CMakeLists.txt
# cd ros_ws dir
$ catkin_make
$ source devel/setup.bash
$ rosrun my_minimal_nodes2 my_minimal_publisher3
```

