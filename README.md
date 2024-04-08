# cabot_teleop_joy package
This package translates `/joy` topic into `/cmd_vel` topic on **ROS 2 Composition**.  
The following 2 compositions are launched.
- joy joy_node
- cabot_teleop_joy joy_to_cmd_vel_composition

## How to use it

```
export ROS_WORKSPACE=$HOME/ros2_ws
mkdir -p $ROS_WORKSPACE/src && cd $ROS_WORKSPACE/src
git clone git@github.com:kimushun1101/cabot_teleop_joy_template.git
rosdep install -riy --from-paths $ROS_WORKSPACE/src/cabot_teleop_joy_template
colcon build --symlink-install
source install/setup.bash
ros2 launch cabot_teleop_joy teleop_joy.launch.yaml
```

## Reference
- [teleop_twist_joy](https://github.com/ros2/teleop_twist_joy)
  : Similar package
- [About Composition](https://docs.ros.org/en/humble/Concepts/About-Composition.html)
  : Concept of ROS 2 Composition
- [Source Code Sample](https://github.com/ros2/demos/tree/humble/composition)
  : Basis of this package
- [ROS 2 Tutorial](https://docs.ros.org/en/humble/Tutorials/Intermediate/Composition.html)
  : Command line interfaces for ROS 2 Components
- [ROS Handson (in Japanese)](https://ouxt-polaris.github.io/ros_handson/rclcpp)
  : Japanese description about ROS 2 Composition

## License
Apache-2.0