# Future-Engineers, HA-LEGACY

# Engineering Materials


# Content
- video: contains the .md file with the link to a video where driving demonstration exists
- schemes: contains several JPEG files with pictures of the electromechanical components used in the vehicle and how they connect to each other.
- t-photos:  contains 2 photos of the team (an official one and one funny photo with all team members)
- v-photos: contains 6 photos of the vehicle (from every side, from top and bottom)
- src: contains code of control software for all components which were programmed to participate in the competition
- other: is for other files and explanations which can be used to understand how to prepare the vehicle for the competition. 

# Introduction 
It is very important to delve into the modules that compose our code in order to understand it in its entirety. The first module is called **fix_g**, its purpose is to avoid the sudden change in the VEX IQ brain's gyroscope values (from 0 to 360), in order to use the directional motor to make the robot to steer in the correct direction if it's a little misaligned. The next module is the **corner** module; it's importance lies in the involvement it has on the robot's ability to make the turn on a corner by the indicating the directional and traction motors how much they should each turn (in degrees) depending on the evaluations inside the module. The **avoid_obstacles** module is in charge of (as implied by the name) avoid the green and red obstacles if it's a challenge round by using the color sensors, the directional, and traction motors. Then, **get_color** is the module that determines the color of the objects by using defined thresholds for each color (red & green) captured by the color sensors on the robot. **monitor_color** evaluates which color is each sensor detecting via the color sensors, this allows the robot to understand where are the obstacles in relation to its position. Last but not least **fw** acts as the module which applies most of the other modules to function; it has many objectives such as moving the robot, evaluating the type of round (open round, challenge round), avoiding objects if present, and steering properly. It is a module which consists of all the other modules presented before, but it nonetheless counts as a module because it used as such in the program. 

The code is uploaded to the robot via VEXcode, available in the vexrobotics.com website, which uses C++ as it's language. 
