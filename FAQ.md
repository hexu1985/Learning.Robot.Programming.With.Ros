
### rosdep init找不到命令
    - Ubuntu20.04下报错：
        ```
        $ sudo rosdep init
        sudo: rosdep：找不到命令
        ```

    - 解决方法
        
        ```
        $ sudo apt install python3-rosdep
        ```

### rosdep init失败 
    - 报错信息
        ```
        $ sudo rosdep init
        ERROR: cannot download default sources list from:
        https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/sources.list.d/20-default.list
        Website may be down.
        ```
    - 解决方法
        + 打开网址：https://site.ip138.com ，在其中搜索raw.githubusercontent.com ，可看到当前解析的IP地址。
        + 打开终端输入指令sudo gedit /etc/hosts，输入用户密码，即可编辑此文档，在其中加入以下语句，其中的151.101.76.133就是上一步中查到的IP地址之一，然后保存并关闭此文档。
            ```
            185.199.110.133 raw.githubusercontent.com
            ```

### rosdep init失败 
    - 报错信息
        ```
        $ sudo rosdep init
        ERROR: default sources list file already exists:
                /etc/ros/rosdep/sources.list.d/20-default.list
        Please delete if you wish to re-initialize
        ```

    - 解决方法

        ```
        $ sudo rm /etc/ros/rosdep/sources.list.d/20-default.list
        ```

### roscore找不到roslaunch

    - 报错信息
        ```
        $ roscore 
        ... logging to /home/hexu/.ros/log/4d7a949c-18d0-11ef-8c7c-c761de3c9ca8/roslaunch-hexu-XPS-13-9360-5237.log
        Checking log directory for disk usage. This may take awhile.
        Press Ctrl-C to interrupt
        Done checking log file disk usage. Usage is <1GB.
        
        Resource not found: roslaunch
        ROS path [0]=/opt/ros/noetic/share/ros
        ROS path [1]=/home/hexu/git/Learning.Robot.Programming.With.Ros/chapter-01/recipe-01/ros_ws/src
        ROS path [2]=/opt/ros/noetic/share
        The traceback for the exception was written to the log file
        ```

    - 解决方法

        ```
        $ sudo apt install ros-noetic-roslaunch
        ```

### rosrun命令不存在

