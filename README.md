# iqr_zs_robot

## DEPEND
- husky
- ur5
- zed2
- d455
- robotiq 85 gripper
- robotiq FT300
- VLP-16
- IMU

## How to use
- compile & environment setup
  ```bash
  cd ~/catkin_ws
  catkin build
  source ~/catkin_ws/devel/setup.bash
  ```

- start robot and sensor 's ros driver
  ```bash
  roslaunch iqr_sz_bringup bringup.launch #You can modify this file to activate different sensors.
  ```
  then, you can view all of the topic
  ```bash
  rostopic list
  ```
- visualization
  ```bash
  roslaunch iqr_sz_description view_robot.launch
  ```
- mapping 
  ```bash
  roslaunch iqr_sz_navigation gmapping_demo.launch viz:=true
  ```
- save map
  ```bash
  roscd iqr_sz_navigation/maps
  rosrun map_serve map_save -f [map_name] 
  ```
- navigation
  ```bash
  roslaunch iqr_sz_navigation amcl_demo.launch viz:=true map_name:=[map_name]
  ```
