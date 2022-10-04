# eecs373_f22_cwc63_lab3

This ROS package depends upon the package `https://github.com/ChenowethColin/ecse373_f22_cwc63_navvis_description`.

This package is ran using `roslaunch lab3 lab3.launch`.

`lab3.launch` has the following parameters:
<br>
&emsp;`use_sim_time` default set to `false`
<br>
&emsp;&emsp;*note that this value is carried through to `navvis_description/launch/display.launch`
<br>
&emsp;`use_xacro` default set to `true`
<br>
&emsp;&emsp;*note that this value is carried through to `navvis_description/launch/display.launch`
<br>
&emsp;`use_gui` default set to `true`
<br>
&emsp;&emsp;*note that this value is carried through to `navvis_description/launch/display.launch`
<br>
&emsp;`old_config` default set to `false`
<br>
&emsp;&emsp;-this value runs off rviz off of `navvis_description/urdf` files (which one depends on `use_xacro`'s value)

If `use_sim_time` is set to `true`, then you will also need to run:
<br>
`rosbag play --clock <full_path_to_bag_file> /tf_trajectory:=/tf`
