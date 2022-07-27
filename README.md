# robot_arm
install and run the arm package on the ROS System(Arduino robot arm)
### **Install the arm package on the system :**

  **- Add the “arduino_robot_arm” package to “src” folder**

	$ cd ~/catkin_ws/src
	$ sudo apt install git
	$ git clone https://github.com/smart-methods/arduino_robot_arm

## - Install all the dependencies

    $ cd ~/catkin_ws
	$ rosdep install --from-paths src --ignore-src -r -y
	$ sudo apt-get install ros-melodic-moveit
	$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
	$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
	$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control

## Compile the package

         $ catkin_make

## run on motors in Rviz
* controlling the motors

      $ roslaunch robot_arm_pkg check_motors.launch


 
 **1. Download the Gazebo program**

   **2.controlling the motors in Gazebo simulation**

    $ roslaunch robot_arm_pkg check_motors.launch
    $ roslaunch robot_arm_pkg check_motors_gazebo.launch
    $ rosrun robot_arm_pkg joint_states_to_gazebo.py

    You may need to change the permission 
	$ cd catkin/src/arduino_robot_arm/robot_arm_pkg/scripts
	$ sudo chmod +x joint_states_to_gazebo.py

## Movelt in Rviz

    Creating the manipulation by using 
      $ roslaunch moveit_setup_assistant setup_assistant.launch

    run Movelt in Rviz
      $ roslaunch moveit_pkg demo.launch

## Movelt in Gazebo

    $ roslaunch moveit_pkg demo_gazebo.launch

