# fROSty-Winter-Episode-2: (the name ...)
Episode 2 content of ROS workshop conducted by ERC

So till now you have learnt how to control our bot and guide it through the maze using your keyboard. But when we are thinking about challenging Moriarty, we can't take any chances! We have to ensure that the bot is able to navigate it's own way through the maze using some clues present at each nodes of the maze. Holmes has deduced the nature of the clues that would be present. According to him, they would be of the form of markers known as ArUco markers. We need to train our bot to identify and process these. But before that, what exactly is this 'ArCuo markers'? Let's find out...

## ArUco Markers
ArUco marker is a grid of black and white squares, typically a 5x5 grid, which looks something like this:

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/ArUco%20marker.png)

In an ArUco marker, black box represents the number 0 and white box represents the number 1. So going by this, let us breakdown the above marker into grid. Also note that ArUco markers have a black border(padding) of 1 unit around them to make their detection easier, so that is neglected below.

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/Grid%20for%20aruco%20marker.png)

Here the second and fourth column are the data bits, and the rest three are parity bits. Parity bits are usually used as a error detection and in this case they also help out in figuring out the orientation of the marker. The Parity1 and Parity3 are even parity bits and Parity2 is odd parity bit. You may read more about parity bits [here](https://en.wikipedia.org/wiki/Parity_bit). But we aren't concerned with parity bits now, so it is fine if you don't understand what they are. 

Finally, coming back to data bits(read them horizontally), the above grid displays the binary number 1010001010, which is 650 in decimal representation.

Let’s see whether you have understood the above info, find out what number does the below ArUco marker represent.(Remember, we only need the second and fourth column to find out)

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Images/Example%20aruco.png)

*Answer: The number represented is 100(in decimal)*

Alright, so now we understand what ArUco markers are, we need to find a way so that they are read by the bot through a camera fitted on it. This can be achieved through OpenCV.

## OpenCV

Firstly you need to install OpenCV in your systems. Please refer to below link for instructions to download OpenCV. Build it from source rather than using pre-built Binaries. This installation can take some time so have patience.

Here's the [link](https://docs.opencv.org/4.5.0/d2/de6/tutorial_py_setup_in_ubuntu.html)





## Detecting ArUco Markers 

Since you have a basic idea of OpenCV, let us see, how can we use it to detect




