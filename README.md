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

The robot used was the Pioneer 3-DX and he was able to navigate the map avoiding obstacles completing his objective in less than 2 minutes. To accomplish this task, the robot uses its 16 distance sensors and a light sensor was added: a light sensor. The light sensor tracks the local irradiance and sends a signal to the robot when it reads over 750 W/m2, which means it is close enough to the floor lamp.

# CONTROL

The robot's navigation around the map is based on a 4-state machine that determines whether it should move forward, turn left, right or stop when it reaches its final objective.

# RESULTS

The video shows the pioneer arriving at the luminous area and stopping, thus completing the proposed challenge.

Click on the image below to watch the video:

[![Video](resources/print.png)](https://www.youtube.com/watch?v=RftRevxZUOE)


**It is the challenges that drive us forward and make us better!**
