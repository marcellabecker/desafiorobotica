# ROBOTIC CHALLENGE - 2021

![banner](https://github.com/marcellabecker/desafiorobotica/blob/webots-2021/resources/banner.png)

Challenge for volunteers at the Robotics and Autonomous Systems Laboratory, at SENAI CIMATEC, 2021.

The objective of this challenge is to develop an autonomous navigation system, so that the robot can reach the illuminated region of the pre-defined map, avoiding all obstacles on the route within 2 minutes. The simulation was performed using Webots software, which is an open source and multi-platform desktop application used to simulate robots.

the challenge is in the repository: https://github.com/Brazilian-Institute-of-Robotics/desafiorobotica

# ORGANIZATION

A organização das pastas é a seguinte:

- `resources` - Resources used in the README.

- `webots_content` - Contains **world**, you can load them inside the Webots simulator.

- `controllers` - Controller used for the challenge

# THE ROBOT

![pioneer](https://github.com/marcellabecker/desafiorobotica/blob/webots-2021/resources/pioneer.png)

The robot used was the Pioneer 3-DX and he managed to navigate the map avoiding obstacles to complete his objective in less than 2 minutes. To accomplish this task, the robot uses its 16 distance sensors to get information from the medium in all directions and a sensor has been added, the light sensor that tracks local irradiance and sends a signal to the robot when it reads more than 750 W / m2, which means it is close enough to the floor lamp that it triggers the STOP.

# CONTROL

The robot's navigation around the map is based on a 4-state machine that determines whether it should move forward, turn left, right or stop when it reaches its final objective.

Thus, the division was made into four cases, they are:

- *FORWARD:* Moves forward and if there is an obstacle ahead starts turning in any direction in order to avoid it.
- *LEFT:* Turn left until object detection is no longer possible;
- *RIGHT:* Turn right until object detection is no longer possible;
- *STOP:* When the light sensor detects the amount of luminosity set (in this case 750 W/m2), the robot must stop.

All distance sensors collect data from the environment that determines whether the robot should move forward or to either side. Each of the 16 distance sensors included in Pionner are found in the robot's control file (challenge_controller.c) and contain weight values for each wheel, which are based on the position of the sensor on the robot and show how its reading influences behavior of the two wheels. In addition, the weight value helps in decision making because, if the reading of any sensor drops below the set minimum value, it means that the robot is close to an obstacle and it must change direction using one of the cases above. In the end it was used to determine the robot behavior at all weight values on each wheel times a speed factor, which is dependent on both the sensor's reading ratio of the minimum distance value.

# RESULTS

The video shows the pioneer arriving at the luminous area and stopping, thus completing the proposed challenge.

Click on the image below to watch the video:

[![Video](resources/print.png)](https://www.youtube.com/watch?v=RftRevxZUOE)


**It is the challenges that drive us forward and make us better!**
