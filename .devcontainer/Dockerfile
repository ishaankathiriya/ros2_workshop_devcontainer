FROM osrf/ros:humble-desktop-full

# Add vscode user with same UID and GID as your host system
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get update \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Switch from root to user
USER $USERNAME

# Update all packages and install commonly used ROS2 packages
RUN sudo apt update && sudo apt upgrade -y && \
    sudo apt install -y \
    ros-humble-gazebo-ros-pkgs \
    ros-humble-ros2-control \
    ros-humble-ros2-controllers \
    ros-humble-gazebo-ros2-control \
    ros-humble-slam-toolbox \
    ros-humble-navigation2 \
    ros-humble-xacro \
    git \
    python3-pip

# Rosdep update
RUN rosdep update

# Source the ROS setup file
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

ENV SHELL /bin/bash
CMD ["/bin/bash"]
