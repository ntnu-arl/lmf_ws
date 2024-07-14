# lmf_ws
This workspace will launch the ORACLE methods on the real-world Learning-based Micro Flyer (NVIDIA Jetson Orin NX board). It uses the [vcstool](https://github.com/dirk-thomas/vcstool) to specify the repositories and branches used.

## Setup

```bash
git clone git@github.com:ntnu-arl/lmf_ws.git
cd lmf_ws
mkdir src
vcs import < lmf.rosinstall
```

## Build

```bash
catkin config -DCMAKE_BUILD_TYPE=Release --blacklist deep_collision_predictor
catkin build
```

## Install

```bash
source devel/setup.bash 
```

## Launch

```bash
roslaunch lmf_launch lmf.launch 
```

In another terminal, follow the instructions [here](https://github.com/ntnu-arl/ORACLE/blob/main/README.md#in-the-real-robot-see-more-info-about-the-robot-here) to launch + start ORACLE.
