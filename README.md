# ecse373_f22_cxj271_navvis_description

**How to run:**

After configureing ROS use the launch file to run as such:
roslaunch navvis_description navvis.launch 
  
**Additional Options:**

1. use_xacro:= true/false
- default=true
- if true, uses the .xacro file as the as the robot_description
- if false, uses the .urdf file as the robot description

2. use_gui:= true/false
- default=true
- if true, uses joint_state_publisher_gui
- if false, uses the joint_state_publisher (no gui)

**Full command with default options:**

roslaunch navvis_description navvis.launch use_xacro:= true use_gui:= true
