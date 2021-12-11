# fROSty-Winter-Episode-2: (The Sign of ArUcos)
Episode 2 of ROS workshop conducted by ERC

So till now you have learnt how to control our bot and guide it through the maze using your keyboard. But when we are thinking about challenging Moriarty, we can't take any chances! We have to ensure that the bot is able to navigate it's own way through the maze using some clues present at each nodes of the maze. Holmes has deduced the nature of the clues that would be present. According to him, they would be of the form of markers known as ArUco markers. We need to train our bot to identify and process these. But before that, what exactly is this 'ArCuo markers'? Let's find out...

## ArUco Markers
ArUco marker is a grid of black and white squares, typically a 5x5 grid, which looks something like this:

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/ArUco%20marker.png)

In an ArUco marker, black box represents the number 0 and white box represents the number 1. So going by this, let us breakdown the above marker into grid. Also note that ArUco markers have a black border(padding) of 1 unit around them to make their detection easier, so that is neglected below.

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/Grid%20for%20aruco%20marker.png)

Here the second and fourth column are the data bits, and the rest three are parity bits. Parity bits are usually used as a error detection and in this case they also help out in figuring out the orientation of the marker. The Parity1 and Parity3 are even parity bits and Parity2 is odd parity bit. You may read more about parity bits [here](https://en.wikipedia.org/wiki/Parity_bit). Below is the order according to which they are calculated.

![Image for parity bits code](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/Parity%20bits%20order.png)

It's fine if you don't understand what parity bits are, as that part is taken care by the computer.

Finally, coming back to data bits(read them horizontally), the above grid displays the binary number 1010001010, which is 650 in decimal representation.

Let’s see whether you have understood the above info, find out what number does the below ArUco marker represent.(Remember, the second and fourth columns are data bits.) You can also cross-check whether 

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/Example%20aruco.png)

*Answer: The number represented is 100(in decimal)*

Alright, so now we understand what ArUco markers are, we need to find a way so that they are read by the bot through a camera fitted on it. This can be achieved through OpenCV.

## OpenCV

OpenCV (Open-Source Computer Vision Library) is an open-source library that includes several hundreds of computer vision algorithms. It helps us in performing various operations on images very easily.

In our task we will be mainly using ArUco, an OpenCV based library for detecting the markers and navigating through the base. Nevertheless, some basic knowledge of OpenCV might be very useful for some of your future projects in Gazebo and Rviz.

### Installation and Setup

* Installing OpenCV </br>
  
  Firstly you need to install OpenCV in your systems. Please refer to this [link](https://docs.opencv.org/4.5.0/d2/de6/tutorial_py_setup_in_ubuntu.html) for instructions to download OpenCV. Build it from source rather than using pre-built Binaries. This installation can take some time so have patience.

  Since we do not require the ROS environment for this section, we recommend you using the **Visual Code Studio** that we installed in Week_0. Using the terminal for practicing code might make reading and editing code a nightmare. We have also provided you with some sample images uploaded in the git folder (images_for_cv2) to practice these commands for yourself.

* Setting up VS code
  1)	Create a folder named opencv_tutorials in your user directory
  2)	Download the folder (images_for_cv2) and transfer it to your Ubuntu desktop and paste it in opencv_tutorials.
  3)	Launch VSC and in the explorer’s tab open the newly created folder and create a .py file to write your practice code.
  4)	Open the Extensions tab on the left side of your screen. Search and install the python extension.

Congrats! Now we are all set and can start with learning OpenCV!

### Module 1: Basic Commands

*	#### Importing the cv2 library </br>
    
    We import OpenCV with the following command: ```import cv2``` </br>
    We also include some other packages which we might be using soon.
    ```import numpy as np```
  
*	#### Reading a saved image on your device </br>

    This method loads an image from the specified file as a NumPy array with each cell as a pixel. </br>
    _Syntax_ – ```cv2.imread( path ,  flag )``` </br>
    _Parameters_ - </br>
                  **path:** A string representing the path of the image to be read. </br>
                  **flag (optional):** It specifies the way in which image should be read. It’s default value is ```cv2.IMREAD_COLOR```.</br>
                  Refer [here](https://docs.opencv.org/3.4/d8/d6a/group__imgcodecs__flags.html) for more details.



## Detecting ArUco Markers 

Since you have a basic idea of OpenCV, let us see, how can we use it to detect




