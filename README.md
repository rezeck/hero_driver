# HeRo: An Open Platform for Robotics Research and Education
![www.verlab.dcc.ufmg.br](https://www.verlab.dcc.ufmg.br/wp-content/uploads/2013/09/SVG_Verlab_900dpi-300x86.png)

This project contributes to an open source ROS-based framework for swarm robotics. We propose an low cost, high availability swarm system that could be printed and assembled multiple times without special knowledge or hardware skills.
<img src="hero_resources/media/images/hero_v2_real.png" width="200">

# Authors:
- [Paulo Rezeck](https://github.com/rezeck)
- [Hector Azpurua](https://github.com/h3ct0r)
- [Maurício Ferrari](https://github.com/mauferrari)

# New Version 2019
- Wheels encoders
- Inertial Motion Unit (IMU)
- General Purpose Bus (I2C/Serial/IO)
- Communication Improves
- Setup via Web Interface
- Small design
- and more...

# Dependencies
- ROS Kinect (http://wiki.ros.org/kinetic/Installation)
- Rosserial (http://wiki.ros.org/rosserial)
- Arduino IDE (to install the firmware)

# How to install HeRo common node
- Using git (or download the zip file) clone this repository into ros workspace.
- Compile with: 
```
$ catkin_make
```
- Fixing package dependencies:
```
$ rosdep install hero_common
```

# How to install the firmware
- Open the arduino IDE.
- Go to preferences:
 - Change the sketchbook location to access the folder firmware.
 - Add (http://arduino.esp8266.com/stable/package_esp8266com_index.json) to Additional Boards Manager URLS.
 - Restart the IDE.
- Go to Sketchbook/hero/firware

## Robots Firmware
- Open the robot code inside the sketchbook.
- Change the essid and password parameter to acess the ROS master.
- Set an ID for each robot.
- Connect HeRo at USB and upload the code.

# How to start the ROS node

- Run the hero_bringup.launch file with:
```
$ roslaunch hero_bringup hero_bringup.launch
```
- Turn on the robots.

## Teleop Demo
- Run the hero_teleop.launch file to control it and set the specific robot id:
```
roslaunch hero_bringup hero_teleop.launch id:=1
```

# Some Videos
[![IMAGE ALT TEXT](http://img.youtube.com/vi/foQDcUG9Arg/0.jpg)](http://www.youtube.com/watch?v=foQDcUG9Arg "Video Title")
