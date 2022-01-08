# Final Task

Here is the final task of this workshop. We hope you have gone through all the episodes and had a great time learning. If you have any doubts you can reach out to us. 

In this task you have to program a bot to autonomously navigate its way out of a maze. Firstly download the maze world file from here(add hyperlink); save it into your world folder of your 'ep3' workspace, and name it as 'final_maze.world'. Next, download the launch file from here(add hyperlink). Save it in you launch folder and name it as final_task.launch.

Here is what you have to do:
The maze will consist of some nodes with only one turn, either right or left. You have to write a code such that the waffle_pi detects where the wall is and turns to the correct direction. You have to use laser scan for this.

Next there will be some nodes where there will be two turns present: right and left. There will be an ArUco marker present at such nodes. You have to read that ArUco marker present and find out its orientation(you can refer episode2 for this), if the orientation is between 0° and 180°, then you have to turn right, else turn right.

Write the code and store the python script in the scripts folder(if not present make one).

Now go to your catkin_ws and run in the terminal:
```
catkin_make
```
Then run:
```
roslaunch ep3 final_task.launch
```
And then run the python script which you have written.

For those of you who manage to solve the maze, at the end of the maze, you will find another bot waiting for your bot, as soon as it detects you, you will see a message printed on the terminal which is the password for your workshop completion certificate.

