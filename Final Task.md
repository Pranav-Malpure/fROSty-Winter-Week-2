# Final Task

So finally we have reached the ultimate task of the workshop.  

![finally](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/W3_Images/benedict-cumberbatch-oh.gif)

We hope you have gone through all the episodes and had a great time learning. If you have any doubts you can reach out to us.

In this task you have to write a code for autonomous navigation of bot to solve maze. As you saw in week2 ArUco will help you to solve maze.
Git clone follwing package. This package is nearly same as the one you saw in week2.
Open the Terminal and run following commands-
```bash
cd ~/catkin_ws/src
git clone -b python2_melodic --single-branch https://github.com/Tejas2910/aruco_detection
cd ~/catkin_ws
catkin_make
```
<img src="Images/Screenshot%20from%202022-01-08%2023-26-41.jpg" width=600 height=300>

## Some points to Remember

final_maze.world is the world file with the code of maze.

Edit follwing line of maze_aruco.launch file 
```bash
<arg name="world_name" value="$(find aruco_detection)/worlds/final_maze.world"/>
```
Run maze_aruco.launch file to launch final_maze.world.

Edit follwing line of spawn_turtlbot3.launch file.
```bash
<arg name="model" default="burger" doc="model type [burger, waffle, waffle_pi]"/>
```
Run spawn_turtlebot3.launch file to spawn burger model. 

As you know, burger model don't have camera sensor. So, we can not detect ArUco with it. 

But, we have edited turtlebot3_burger.urdf.xacro and turtlebot3_burger.gazeno.xacro files to add camera plugin to it. So, burger model can also detect ArUco.
You can compare these files with earlier ones to see, how can you add different sensors to your robot model.

Cool!!

In scripts folder, you will see one more file navigator.py 
We have given helper code in it, you have to edit this file to complete task2
