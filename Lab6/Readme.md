# Choreographing Movement
**List the names and NetID for your partners here.**

Hongyu Shen hs692, Sylvie Chen xc455, Haohua Liu hl766, Tsung-Yin Hsieh th542, Jonathan Tan jmt362

It is about time to have a functioning mobile robot! Starting from this lab, you should prioritize either robot building and/or study design. 

## Prep
### Watch the following tutorials:
- [How to crimp wires](https://www.youtube.com/watch?v=SaU00MMjzn0&ab_channel=GrizzlyBuilds)

- [Beginner's Guide on Soldering](https://www.makerspaces.com/how-to-solder/)


- [How to Solder Wires Together](https://youtu.be/NSqPHQ1zQco)



### For this lab, you will need:
1. Your laptop
2. Cardboard
3. Utility knife
4. Your hoverboard base

### Deliverables for this lab are: 

0. Photos of your robot prototype
1. A video of your robot moving around
2. A sketch of a series movements based on your final project
3. A video showing your robot perform the movements in item #2.
4. Reflect upon your design, what would you do differently?


## Lab Overview
For this assignment, you are going to:

A) [Build your chassis](#part-a-build-your-chassis)

B) [Move it around](#part-b-move-it-around)

C) [Plan a movement](#part-c-plan-a-movement)

D) [Optional Spinning your LiDAR](#part-d-optional-spinning-your-LiDAR)

Labs are due on Tuesdays before class. Make sure this page is linked to on your main class hub page.

## Part A. Build your chassis
If you haven't already, now is a good time to actually mockup a low fidelity version robot for your final project. At least, you should have a chassis that safely host all the hardware you have (ODrive, wheels, battery, etc).

Feel free to use any material we have in lab to build your chassis. Things you might find useful are cardboard, gluegun, zip ties, duo locks, etc. 

## Part B. Move it around
Once you build your chassis, test it out! Power on your hoverboard and connect your controller. Drive your robot around! (Take a video while you do that!)

A few questions to consider:
- when your robot accelerate, is the chassis stable?
- what are all the possible motions (action space) your robot can perform? (e.g. rotating in place, moving foward/backward, ...)
- reflect on your design and think what would you do differently next time.

## Part C. Plan a movement
Based on your scenario, sketch out a sequence of movement in a storyboard format. 
Then, control your robot to execute that sequence of movement. (Take a video while you do that!)


## Part D. Optional spinning your LiDAR
If you plan to use LiDAR for your final project, or are simply curious about how it works, let's set it up!

```
# Install LiDAR SDK
# In your RPi terminal
sudo apt install cmake pkg-config
cd ~
git clone https://github.com/YDLIDAR/YDLidar-SDK.git
cd YDLidar-SDK
mkdir build
cd build
cmake ..
make
sudo make install
```

```
cd ~/mobilehri_ws/src/mobilehri2023
git checkout ydlidar_ros2_driver
cd ~/mobilehri_ws
colcon build

chmod 0777 src/ydlidar_ros2_driver/startup/*
sudo sh src/ydlidar_ros2_driver/startup/initenv.sh

```
Now, plug in your LiDAR.
```
# start your LiDAR
source install setup.bash
ros2 launch ydlidar_ros2_driver ydlidar_launch.py 
```

To visualize your LiDAR reading, open foxglove studio in vnc viewer. Then, click 3D in the left panel.

### Again, deliverables for this lab are: 
We finished connecting all the wires for this robot, but we got USB interface problem on our Odrive, so we cannot move our robot now.
We asked the TA, and he said we can upload the video after spring break. We will finish it once we solve the hardware problem.

<img width="650" alt="Odrive Interface Problem" src="https://user-images.githubusercontent.com/112031955/228399014-35484025-a3f0-4f98-aa0f-683a44c9675f.png">

0. Photos of your robot prototype

<img src="https://user-images.githubusercontent.com/112031955/236503434-1dcba084-0ab7-422d-b5b4-063940e4c280.jpeg" width="500">

<img src="https://user-images.githubusercontent.com/112031955/236503458-00a6ae48-c09b-4f03-830f-1817dbac4f0a.jpeg" width="500">

1. A video of your robot moving around

https://user-images.githubusercontent.com/112031955/236505838-fb6bf9d2-16de-4e49-a54d-ebaf13609030.mp4

2. A sketch of a series movements based on your final project
![IMG_E0004DEA47CF-1](https://user-images.githubusercontent.com/112031955/228397945-4ee79d70-2932-4536-a2d3-663b88bb0a38.jpeg)

3. A video showing your robot perform the movements in 2.

https://user-images.githubusercontent.com/112031955/236503506-2f64ada7-0281-4b74-a294-9cca4ea77b0b.mp4

4. Reflect upon your design, what would you do differently?

First, the current design is just a prototype using cardboard, we would redesign the appearance of this robot to make it more approachable and attractive. Second, the movement of the robot is a little bit aggressive. We should think about how the users can interact with the robot easily by changine the moving behavior of the robots or adding more instructions for users. 


