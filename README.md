<img src="udacity_banner.jpg" height ="20">

### Robotics Software Engineer - Nanodegree

# Project 01 (of 05) : Build My World 
## Directory Structure
```
.Build_My_World                 # Build_My_World package
├── CMakeLists.txt              # compiler instructions  
├── model                          
│   ├── building                # model of environment
│   │   ├── model.config
│   │   └── model.sdf
│   │── robodog                 # model of robot
│   │  ├── model.config
│   │  └── model.sdf
│   └── RoboLeg.STL             # CAD file of Robot's leg (made in SolidWorks)  
├── script
│   └── hello.cpp               # Gazebo World plugin C++ script
├── world
│    └── world1.world           # Gazebo World file (contains the above models) 
├── output
│   └── output.PNG
├── README.md 
├── LICENSE
└──
```



## Project Goals
Designing a Gazebo world which includes building, custom models, Gazebo online library model.

Writing a custom C++ plugin which prints message ('Welcome to Avadhoot's world') in the terminal upon launching the gazebo world.




## Output 
<img src="output/output.PNG">


## Environment
Tested on Ubuntu 16.04.6 LTS, ROS Kinetic, Boost 1.58

## Setup and run
#### 1. Update the Workspace image
```
$ sudo apt-get update && sudo apt-get upgrade -y 
```

#### 2. Clone the files in /home/workspace
```
$ cd /home/workspace/
$ git clone https://github.com/Avadhoot94/Build_My_World.git
```
#### 3. Create a build directory and compile the code
```
$ cd /home/workspace/Build_My_World/
$ mkdir build
$ cd build/
$ cmake ../
$ make
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/Build_My_World/build
```

#### 4. Launch the world file in Gazebo to load both the world and the plugin
```
$ cd /home/workspace/Build_My_World/world/
$ gazebo world1.world
```
