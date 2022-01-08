# Final Task

So finally we have reached the ultimate task of the workshop.  

![finally](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/W3_Images/benedict-cumberbatch-oh.gif)

We hope you have gone through all the episodes and had a great time learning. If you have any doubts you can reach out to us.

In this task you have to program a bot to autonomously navigate its way out of a maze. Firstly download the maze world file from [add hyperlink](addhyperlink); save it into your world folder of your 'ep3' workspace, and name it as 'final_maze.world'. Next, download the launch file from [add hyperlink](mmm). Save it in you launch folder and name it as final_task.launch.


Here is what you have to do:
Once you launch the task, you will see a maze with a waffle_pi bot at its centre. Your objective is to write a program for the bot to get out through the exit. The bot has to move autonomously. The maze consist of some ArUcos present at some of the turns. You have to read that ArUco marker present and find out its orientation(you can refer episode2 for this), if the orientation is between 0° and 180°, then you have to turn right, else turn right. Refer to episode 3 contents to make the bot autonomous.

To help you with the code, [here](nj) is a helper code, you just have to fill the remaining portions of the code.
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

