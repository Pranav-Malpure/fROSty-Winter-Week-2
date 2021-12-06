# fROSty-Winter-Episode-2:
Episode 2 content of ROS workshop conducted by ERC

So till now you have learnt how to control our bot and guide it through the maze using your keyboard. But when we are thinking about challenging Moriarty, we can't take any chances! We have to ensure that the bot is able to navigate it's own way through the maze using some clues present at each nodes of the maze. Holmes has deduced the nature of the clues that would be present. According to him, they would be of the form of markers known as ArUco markers. We need to train our bot to identify and process these. But before that, what exactly is this 'ArCuo markers'? Let's find out...

## ArUco Markers
ArUco marker is a 5x5 grid of black and white squares which looks something like this:

![This is an image](https://github.com/Pranav-Malpure/fROSty-Winter-Week-2/blob/main/Aruco%20image.jpeg)

Let us breakdown this marker into grid. Also note that ArUco markers have a black border of 1 unit around them.

