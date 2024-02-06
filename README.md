Step 1: Build the docker file
Step 2: Call the docker image by running following commands
||
docker run -it --rm -p 10000:10000 -e DISPLAY=172.30.0.1:0 unity-robotics:pick-and-place /bin/bash
source /opt/ros/melodic/setup.bash
source /catkin_ws/devel/setup.bash
roslaunch niryo_moveit part_3.launch
Object Estimation:---p
docker run -it --rm -p 10000:10000 -e DISPLAY=172.30.0.1:0 unity-robotics:pose-estimation /bin/bash
||
Step 3: Source the unity file by adding it as project and run it. Use port 10000:127.0.0.1 as communication port

Step 4: Run Scenario2 and Scenario 3

Step 5: Its not device agnostic, but I will provide a docker image in future

Soure ROS2, go the the packages and type run sphero sphero 
You will see some values wait until the values are zero
Now dont disturb the sphero and run unity project
If you rotate anticlockwise, it will enter the keystroke P, if you roatate clockwise it will enter keystroke O. and if you roate along the axis it will enter keystroke I. 
Make sure you dont have ant text editor open and the ROS2 window and unity window are dispalyed at same time. Otherwise it will fail to register key strokes. and also system crashes have been noticed when you haev notepad/text editor running.
