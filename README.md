# Steps of Install robot arm pkg

1. Create a workspace by using catkin_make
	- mkdir -p ~/catkin_ws/src
	- cd ~/catkin_ws/
	- catkin_make
2. Add the “arduino_robot_arm” package to “src” folder
	- cd ~/catkin_ws/src
	- git clone https://github.com/smart-methods/arduino_robot_arm.git 
	- cd ~/catkin_ws
3. Install all the dependencies 
	- rosdep install --from-paths src --ignore-src -r -y
	- sudo apt-get install ros-kinetic-moveit
	- sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui
	- sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
	- sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
	- sudo nano ~/.bashrc
	- at the end of the (bashrc) file add the follwing line :
		(source /home/<your_virtual_OS_name>/catkin_ws/devel/setup.bash)
		then 
		ctrl + o
		source ~/.bashrc
4. Compile the package
	- catkin_make
5. Launch robot arm pkg
	roslaunch robot_arm_pkg check_motors.launch


