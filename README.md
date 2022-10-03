# ecse373_f22_cxj271_navvis_description

**How to run:**

After configureing ROS use the launch file to run as such:
roslaunch navvis_description navvis.launch 
  
**Additional Options:**

1. use_xacro:= true/false
- default = false
- if true, uses the .xacro file as the as the robot_description
- if false, uses the .urdf file as the robot description

2. use_gui:= true/false
- default = true
- if true, uses joint_state_publisher_gui
- if false, uses the joint_state_publisher (no gui)

3. use_new_robot:= true/false
- default = "false"
- should always be false when running roslaunch navvis_description navvis.launch
- this was added for the new lab to add a component to the navvis robot. See the readme for the ecse373_f22_cxj271_navvis_explore repository

4. use_robot_state_publisher:= true/false
- default = "true"
- if true: creates the robot_state_publisher and joint_state_publisher nodes
- if false: creates the static_transform_publisher nodes for the three wheels

5. config_file_name = "<filename>"
- default = "config.rviz"
- sets the filename for the config file
- There are currently 3 options: 
  1. config.rviz
    - basic .rviz config file and should be used if use_new_robot = "false"
  2. config_w_laser_nomap.rviz
    - if use_new_robot = "true":
      - Shows the lasers but user will need to change the fixed frame and the target frame to show the map
    - if use_new_robot = "false"
      - Shows the "Laserscan" in the display panel but lasers cannot be seen in the visual panel
  3. config_w_map.rviz
    - **CANNOT BE USED IF use_new_robot = "false"**
    - Shows the map for the 5th floor of Glennan, the navvis robot roaming around, and the 3D lidar readings
    
6. use_external_clock := true/false
- default = "true"
- In the rviz node, sets the param "/use_sim_time" to be true or false


**Full command with default options:**

roslaunch navvis_description navvis.launch use_xacro:= true use_gui:= true use_new_robot:= false use_robot_state_publisher:=true config_file_name:="config.rviz" use_external_clock:=true
