# Pioneer Robot Base Package
===============

Repo forked from eborghi10/my_ROS_mobile_robot (https://github.com/eborghi10/my_ROS_mobile_robot) - amazing repo that you should definitely use as the base for implementing ros_control on a differential drive robot. It takes a while to figure out what's going on, but nevertheless a great resource, written by a far superior C++ programmer than me.

I adapted the code to work with a Pioneer3AT 4 wheel, differential drive robot. I am using a Teensy 3.2 microcontroller to interface with the Pioneer motor control board (MCB). See https://github.com/Gregory-Baker/pioneer3at-teensy-ros for the Teensy sketch, which is based on eborghi10's arduino and ESP32 sketches in the aforementioned repo.

eborghi10's implementation uses effort controllers and PID loop from ros_control. I replaced this with PID onboard the microcontroller itself. My implementation is not neccessarily superior, it's just how I decided to do it.

## Test

To run the `ros_control` node, use:

```bash
$ roslaunch pioneer_base hw_control.launch
```

