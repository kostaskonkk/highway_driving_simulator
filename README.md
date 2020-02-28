# Highway Simulator for ROS in Gazebo

This is a simulation of highway driving with three driveable Prius cars in [gazebo 9](http://gazebosim.org) with sensor data being published using [ROS melodic](http://wiki.ros.org/melodic/Installation)
The first of the three vehicles is equipped with a LIDAR, front and rear camera, and eight RADAR sensors, while the other two cars have no sensors onboard.

The car's throttle, brake, steering, and gear shifting are controlled by publishing a ROS message.
A ROS node allows driving with a gamepad or joystick.

In addition to the three Prius cars, there is a bus and a truck at the oppposite lane, which follow predetermined straight paths.

# Video

![Video of the simulation environment](https://github.com/kostaskonkk/highway_driving_simulator/raw/master/videos/overtakes.gif)
<!--A video and screenshots of the demo can be seen in this blog post: https://www.osrfoundation.org/simulated-car-demo/-->

<!--![Prius Image](https://www.osrfoundation.org/wordpress2/wp-content/uploads/2017/06/prius_roundabout_exit.png)-->


# Recommended

* Joystick drivers which create links to `/dev/input/js0`, `/dev/input/js1`, `/dev/input/js2`

This has been tested with the Logitech F710 in Xbox mode. If you have a different joystick you may need to adjust the parameters for the very basic joystick_translator node: https://github.com/kostaskonkk/highway_driving_simulator/blob/master/car_demo/nodes


An [RVIZ](http://wiki.ros.org/rviz) window will open showing the car and sensor output.
A gazebo window will appear showing the simulation.
Either use the controller to drive the prius around the world, or click on the gazebo window and use the `WASD` keys to drive the car.

If using a Logitech F710 controllers:

* Make sure the MODE status light is off
* Set the swtich to XInput mode
* The right stick controls throttle and brake
* The left stick controls steering
* Y puts the car into DRIVE
* A puts the car into REVERSE
* B puts the car into NEUTRAL
