# AI_TASK4_SMART_METHODS-
This work is for my fourth task in the AI route at [Smart Methods'](https://s-m.com.sa/c12_in.php) training program.

## Task description 
Using SLAM map to launch Autonomous Navigation.

## Task Steps
1- Launch the simulation world normally using 
```
export TURTLEBOT3_MODEL=burger 
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
2- Run the navigation node in another terminal using
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```
3- In RViz click on **2D Pose Estimate** and click on the map where the robot is in the gazebo simulation(actual location).
point the green arrow where the robot is facing.

![2D Pose Estimate](https://user-images.githubusercontent.com/85564881/126046532-e670234c-1e8e-4162-8514-1ef11f60260d.gif)

4- Launch the operating node using `roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch` and move the robot a little to accurately determine the robot's location. 
even if you did not click on the robot's location accurately in the pervious step, moving the robot around in this step will precisely determine the location anyways.

![](https://user-images.githubusercontent.com/85564881/126046718-68bd2966-0eed-472d-96c8-ea31f0922c0c.gif)

5- Now that the robot location is determined, we can launch the navigation and the robot will automatically go to the pointed location without bumping into obstacles.
To do this, we click on **2D Nav Goal** in RViz and just like previously, click on the location where you want the robot to go and point the arrow where you want the robot to face when it reached the location.

![2d Nav Goal](https://user-images.githubusercontent.com/85564881/126047175-ff53c68f-72d6-479f-ad30-33786fb8d516.gif)

and with this we finished the task.
