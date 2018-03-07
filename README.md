[micro-ROS](https://cordis.europa.eu/project/rcn/213167_en.html) puts ROS2 onto microcontrollers, making them first class participants of the ROS 2 environment.


The micro-ROS architecture is being built with software modularity in mind and is
 decribed below:
```
+-------------------------------------------------------------+
|               embedded application layer                    |
+-------------------------------------------------------------+
|             micro-ROS client library (urcl)                 |
                e.g.: tf, lifecycle, executors, etc.          |
+-------------------------------------------------------------+
|             micro-ROS middleware interface (urmw)           |
+-------------------+---------------------+-------------------+
|    middleware 1   |     middleware 2    |   middleware 3    |
| (e.g. micro-RTPS) |     (e.g. mqtt)     |                   |
+-------------------+---------------------+-------------------+
|      Real-Time Operating System (RTOS) abstractions         |
+------------------+------------------+-----------------------+
|         RTOS 1   |       RTOS 2     |        RTOS 3         |
|     (e.g. NuttX) |    (e.g. RIOT)   |    (e.g. Zephyr)      |
+------------------+------------------+-----------------------+
|                         hardware                            |
+-------------------------------------------------------------+
```
(*replace this by a clickable SVG in the future. The SVG should facilitate quick access to the different abstractions in micro-ROS*)

### ROS 2 and its architecture
ROS 2 is the second generation of an open-source, meta-operating system for your robot maintained by the [Open Source Robotics Foundation](http://osrfoundation.org) (OSRF).
Its  architecture is described below:

```
+-----------------------------------------------+
|                   user land                   |
+-----------------------------------------------+
|              ROS 2 client library (rcl)       |
+-----------------------------------------------+
|             middleware interface (rmw)        |
+-----------------------------------------------+
| DDS adapter 1 | DDS adapter 2 | DDS adapter 3 |
+---------------+---------------+---------------+
|    DDS impl 1 |    DDS impl 2 |    DDS impl 3 |
+---------------+---------------+---------------+
```
