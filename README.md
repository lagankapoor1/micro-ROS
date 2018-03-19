[micro-ROS](https://cordis.europa.eu/project/rcn/213167_en.html) puts ROS2 onto microcontrollers, making them first class participants of the ROS 2 environment.

This is an Open Source project, and you can collaborate both here (through issues and PR's, as usual) and on ROS Discourse, of course.

The micro-ROS architecture is a work in progress, and while we do have some ideas, for now, lets just say that it's modular and built from the following ingredients:
  
 - A Real-Time Operating System (RTOS). This includes at least NuttX, and possibly others
 - An embedded middleware, at least micro-RTPS (a.k.a. DDS-XRCE), maybe others
 - The ROS client library

From the level of ROS onwards, we strive to re-use as much as possible from ROS2, and be as compatible with it as possible. In some areas, we will probably do custom implementations optimized for resource use. This will definitely include TF, and maybe other areas such as scheduling. These optimized implementations may also be interesting for use with "normal" ROS2.

We'll update this README as we proceed. For now, you can check out our work on
 - RTOS: https://github.com/microROS/NuttX
 - Reference hardware: https://github.com/microROS/hardware
 - Build infrastructure for embedded development using docker: https://github.com/microROS/docker

