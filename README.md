ROS安装在线描述链接: https://wiki.ros.org/indigo/Installation/Ubuntu
ROS机器人编程 原理与应用 示例代码
- https://github.com/wsnewman/learning_ros
- https://github.com/wsnewman/learning_ros_external_packages

```
$ git clone https://github.com/wsnewman/learning_ros.git
$ git clone https://github.com/wsnewman/learning_ros_external_packages.git
```

### 如何在 Ubuntu 18.04 上安装 ROS Melodic 的详细过程：

- 设置 ROS 镜像：

    ```
    $ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    ```

- 设置密钥：

    ```
    $ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
    ```

    或者

    ```
    $ sudo apt install curl # if you haven't already installed curl
    $ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
    ```

- 安装 ROS：

    ```
    $ sudo apt update && sudo apt install dpkg

    # Ubuntu 20.04
    $ sudo apt install ros-noetic-desktop-full

    # Ubuntu 18.04
    $ sudo apt install ros-melodic-desktop-full
    ```

- 初始化 rosdep：

    ```
    $ sudo rosdep init 
    $ rosdep update
    ```

- 设置环境变量：

    ```
    # Ubuntu 20.04
    $ echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc source ~/.bashrc

    # Ubuntu 18.04
    $ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc source ~/.bashrc
    ```

    或者每次手动执行

    ```
    # Ubuntu 20.04
    $ source /opt/ros/noetic/setup.bash

    # Ubuntu 18.04
    $ source /opt/ros/melodic/setup.bash
    ```

- 安装 Python 工具：

    ```
    # Ubuntu 20.04
    $ sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

    # Ubuntu 18.04
    $ sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential
    ```

- 安装小海龟：

    ```
    # Ubuntu 20.04
    $ sudo apt install ros-noetic-turtlesim

    # Ubuntu 18.04
    $ sudo apt install ros-melodic-turtlesim
    ```

接下来，您就可以在终端中运行以下命令来启动小海龟：

    ```
    # tty1
    $ roscore

    # tty2
    $ rosrun turtlesim turtlesim_node

    # tty3
    $ rosrun turtlesim turtle_teleop_key
    ```


### 如何在 Ubuntu 20.04 上安装 ROS Noetic 的详细过程：

- 设置 ROS 镜像：

    ```
    $ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    ```

- 设置密钥：

    ```
    $ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
    ```

    或者

    ```
    $ sudo apt install curl # if you haven't already installed curl
    $ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
    ```

- 安装 ROS：

    ```
    $ sudo apt update && sudo apt install dpkg
    $ sudo apt install ros-noetic-desktop-full
    ```

- 初始化 rosdep：

    ```
    $ sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
    $ sudo rosdep init 
    $ sudo rosdep fix-permissions
    $ rosdep update
    ```

- 设置环境变量：

    ```
    $ echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc source ~/.bashrc
    ```

    或者每次手动执行

    ```
    $ source /opt/ros/noetic/setup.bash
    ```

- 安装小海龟：

    ```
    $ sudo apt install ros-noetic-turtlesim
    ```

接下来，您就可以在终端中运行以下命令来启动小海龟：

    ```
    # tty1
    $ roscore

    # tty2
    $ rosrun turtlesim turtlesim_node

    # tty3
    $ rosrun turtlesim turtle_teleop_key
    ```

