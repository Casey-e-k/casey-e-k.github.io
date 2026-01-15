---
layout: single
title: Autonomous Machine Learning Detective
permalink: /docs/projects/auton-ml-det/
sidebar:
  nav: "docs"
classes: wide
author_profile: true
---

I worked in a team on this project.

**Objective:** develop an autonomous detective that can drive around in a simulation and obey traffic laws while reading billboards containing clues to solve a crime.

**Example Activities:** developed a line following robot in Gazebo using computer vision, created a GUI using PyQt and implemented a Homography based tracker using SIFT, built a Neural Network (NN) from scratch, implemented pedestrian avoidance functionality, trained a CNN to read license plates.

**Tools/Concepts/Skills:** Linux (Ubuntu), Terminal, Gazebo simulator, ROS, Python, PyQt, Computer Vision, Machine Learning, Neural Networks, SIFT, Google Colab, VSCode, how to keep a logbook.

Simulated environment map:

<img width="741" height="449" alt="image" src="https://github.com/user-attachments/assets/bdb0fe22-c4e2-4b5a-bf79-b2917b44a6e2" />

view from the car's POV camera:

<img width="422" height="241" alt="image" src="https://github.com/user-attachments/assets/69b8cb85-b858-47ea-9a28-5cebb6840959" />

Software diagram of the finite state machine:

<img width="639" height="353" alt="image" src="https://github.com/user-attachments/assets/42d4db71-7de6-458e-ae1c-626ac3d16505" />

### My favourite contribution: Pedestrian Detection

Part of the competition involves driving through a crosswalk where a pedestrian is periodically crossing. My job was to ensure we never hit the pedestrian. My strategy was to drive the car forward, looking at the bottom of the car's POV camera input and using a mask to scan for the red line just before the pedestrian crossing. Once the car sees the red line ahead of the crosswalk, it is programmed to stop. I then begin sampling images a short distance apart (about 6 to 10 loops of the ROS callback function - after testing different intervals). I processed the images by blurring them, converting them to grayscale then to black and white, and then subtracted their pixel values from each other (absolute value so I didn’t have any negative pixel values - dependent on whether the pedestrian appeared in the first or second image). I then summed the total number of pixels in that absolute-difference image and compared it to a threshold (chosen from numerous observations) to decide if a pedestrian was present or not.

Example of this background subtraction:

<img width="637" height="334" alt="image" src="https://github.com/user-attachments/assets/6490812a-6303-4af5-ab20-293a3ec57fbd" />

The image sampling and background subtraction process is repeated with new pairs of images every 16 loops until the threshold is been met (i.e. the pedestrian crossed) and then the robot resumes driving. (The number of loops was chosen based on the timing it resulted in). I tried using the opposite logic - go if the robot doesn't see the pedestrian - but quickly realized that the pedestrian crosses very quickly once it has decided to cross and the robot would potentially hit it without for sure knowing that it would be off the road for long enough for the robot to pass and I can only know this if I have just seen it cross since it pauses after crossing.

Full pedestrian detection algorithm:

<img width="803" height="680" alt="image" src="https://github.com/user-attachments/assets/433aa617-8289-49c4-bb52-54beb5b1bd8f" />

Some code snippets:

<img width="632" height="499" alt="image" src="https://github.com/user-attachments/assets/85ebb626-e2e4-42f3-9346-e1ad81a32619" />

<img width="743" height="652" alt="image" src="https://github.com/user-attachments/assets/f6df7734-07a3-4911-b47c-90fb0494d565" />



