


## Discovering TFs with RViz


In ROS, a TF is the transformation between two frames in 3D space. TFs will be used to track the
different coordinate frames of a ROS robot (or system with multiple robots) over time. They are used everywhere and will be the backbone of any robot you create.




In your terminal, type the following command:
```bash
sudo apt install ros-humble-urdf-tutorial
```




## Starting Rviz with a robot model


The urdf_tutorial package contains a launch file, named display.launch.py, that will start RViz and
load a robot model into it


```bash
cd /opt/ros/humble/share/urdf_tutorial/urdf/

ls
```


You can now start a robot model in RViz by launching the display.launch.py file and add the path to the robot model with an additional model argument after the launch file:


```bash
ros2 launch urdf_tutorial display.launch.py model:=/opt/ros/humble/share/urdf_tutorial/urdf/07-physics.urdf
```


A **Unified Robot Description Format (URDF)** file is basically the description of a robot model. For now, all we want to do is to visualize one. In the urdf folder, you can find several robot model files:

You will get two windows: the main one (RViz) with the robot model, and a Joint State Publisher
window with some cursors. 


Star Wars fans should know who this robot resembles :)




## What are TFs and Links?


There are two main parts in any robot model -> Links and TFs. Let's visualize both



### Links

Look at the left side of the RViz window, there, you will see, in blue bold letters,
RobotModel and TF


Disable TF, keep RobotModel, and expand the menu. There, you can find a submenu called Links.


Check and uncheck some boxes. As you can see from this menu, a link is one rigid part (meaning one solid part with no articulation) of the robot.  In ROS, a robot model consists of a
collection of rigid parts put together.

These rigid parts alone cannot do anything, and hence they are **connected.** 

To know how they are connected and how they move relative to each other, is where TFs come in.



### TFs

Now, check the TF box and uncheck the RobotModel.

The axes you see here (red, green, and blue coordinate systems) represent the frames, or basically the origin of each link of the robot.

- X axis (red) pointing forward
- Y axis (green) pointing 90 degrees to the left
- Z axis (blue) pointing up


To summarize, TFs determine how one rigid part is placeed relative to another rigid part. Additionally, TFs also determine whether the two parts are moving and **how** are they moving - Translational, Rotational, etc.



### The /tf topic & Visualising TFs


```bash
ros2 topic echo /tf --once
```


For each robot, you can visualize the complete TF tree in a simplified way, so that you can see all the relationships between all the TFs.


First, you need to install the tf2-tools package:
```bash
sudo apt install ros-humble-tf2-tools
source ~/.bashrc
```

now, run:
```bash
ros2 run tf2_tools view_frames
```






