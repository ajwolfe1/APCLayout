# Homework 1 ROS2 Notes

### To Launch World

<pre>
source /opt/ros/humble/setup.bash
</pre>

<pre>
export WEBOTS_HOME=/mnt/c/Program\ Files/Webots
</pre>

<pre>
git clone https://github.com/ajwolfe1/APCLayout/
</pre>

<pre>
cd APCLayout
sudo colcon build
</pre>

<pre>
source install/setup.bash
</pre>

<pre>
ros2 launch webots_ros2_homework1_python f23_robotics_1_launch.py
</pre>

### Door and Light Edits
Reset all doors to zero(closed) before closing, otherwise, you will +/- 1.5 depending on the sign to open(from whatever the number is now)

Door(1) position->1.5 open ; 0 close

Door(2) position->-1.5 open ; 0 close

Door(3) position->-1.5 open ; 0 close

Door(4) position->-1.5 open ; 0 close

Door(10) position->1.5 open ; 0 close

Door(16) position->1.5 open ; 0 close

Door(20) position->-1.5 open ; 0 close

Door(21) position->1.5 open ; 0 close

Door(22) position->-1.5 open ; 0 close

Door(23) position->1.5 open ; 0 close

Door(24) position->1.5 open ; 0 close

Door(25) position->-1.5 open ; 0 close

Door(26) position->1.5 open ; 0 close

Door(27) position->1.5 open ; 0 close

Door(28) position->1.5 open ; 0 close

Door(29) position->-1.5 open ; 0 close

Door(30) position->-1.5 open ; 0 close

Door(31) position->1.5 open ; 0 close

For lights go to the Point Light Node that corresponds with the DoubleFlourescent lights that you want to increase/decrease and increase/decrease the intensity

### TO INSTALL PACKAGE FOR ASSIGNMENT 

1. Set up environment variables for ROS. Make sure to replace '/home/rpi/shared' with your own shared folder location
<pre>
source /opt/ros/humble/setup.bash
</pre>
Also do any Windows or Mac specific setup

For example in Mac...
<pre>
export WEBOTS_HOME=/Applications/Webots.app
python3 local_simulation_server.py
</pre>

For example in windows...
<pre>
export WEBOTS_HOME=/mnt/c/Program\ Files/Webots
</pre>

2. Fork your own repository of f23_robotics (using web interface)

3. Clone your fork
<pre>
git clone <your github url for this repository>
</pre>

4. Make the package (for python, it really just installs the files
<pre>
cd f24_robotics
colcon build
</pre>

5. Set up variables to use the package you just created
<pre>
source install/setup.bash
</pre>

6. Start webots simulation with connect back to ROS in the virtual machine
<pre>
ros2 launch webots_ros2_homework1_python f23_robotics_1_launch.py
</pre>


### TEST THE CONNECTION BETWEEN ROS2 AND WEBOTS

Test the connection between webots and ROS, use a ROS based ASCII keyboard to move the simulated robot in Webots

1. Open another terminal

2. Redo the source commands (you can add to your bash to execute it automatically each time) 
<pre>
source /opt/ros/humble/setup.bash
source install/setup.bash
</pre>

3. Run the ROS-based keyboard
<pre>
ros2 run teleop_twist_keyboard teleop_twist_keyboard
</pre>


### TO VISUALIZE LASER DATA

1. Open another terminal

2. Redo the source commands (you can add to your bash to execute it automatically each time) 
<pre>
source /opt/ros/humble/setup.bash
source install/setup.bash
</pre>

3. Run the ROS-based keyboard
<pre>
ros2 run teleop_twist_keyboard teleop_twist_keyboard
</pre>
<pre>
  rviz2
</pre>

### RUN SAMPLE CONTROLLER

<pre>
ros2 run webots_ros2_homework1_python webots_ros2_homework1_python
</pre>
