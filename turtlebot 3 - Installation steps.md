
## Create workspace

```bash
mkdir -p ~/turtlebot3_ws/src
cd ~/turtlebot3_ws/src
```


## Clone all repos

```bash
# Clone TurtleBot3 messages
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git

# Clone main TurtleBot3 package
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3.git

# Clone TurtleBot3 simulations
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

# Clone the online SLAM package
git clone https://github.com/ishaankathiriya/turtlebot3_online_SLAM.git
```



## Install additional dependecies

```bash
cd ~/turtlebot3_ws
rosdep update
rosdep install -i --from-path src --rosdistro humble -y
```


## Build the workspace

```bash
cd ~/turtlebot3_ws
colcon build
```


Also, execute the following commands 
```bash
echo "source ~/turtlebot3_ws/install/setup.bash" >> ~/.bashrc
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
echo "export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:~/turtlebot3_ws/src/turtlebot3_simulations/turtlebot3_gazebo/models" >> ~/.bashrc
source ~/.bashrc
```





----

###### Prepared By: Ishaan Kathiriya
[linkedin](https://www.linkedin.com/in/ishaan-kathiriya)


