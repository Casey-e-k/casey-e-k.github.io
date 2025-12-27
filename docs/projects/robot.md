---
layout: single
title: Autonomous Mario Kart Robot
permalink: /docs/projects/robot/
sidebar:
  nav: "docs"
classes: wide
author_profile: true
---
Along with 3 other students, I designed and built an autonomous robot capable of racing a real-life Mario Kart course with mystery blocks to collect, bombs to avoid, bananas to drop, and several shortcuts and obstacles. My team made it to quarter finals of the competition and were interviewed by the news in the following clip:

[News Coverage](https://www.ctvnews.ca/vancouver/article/ubc-students-bring-mario-kart-to-life-with-robotics-competition/)

The competition involved multiple rounds where two robots would race each other on the same track, pictured below.

<img width="789" height="408" alt="image" src="https://github.com/user-attachments/assets/a786d718-7f57-4507-9e65-056d981f31af" />

Each mystery block collected awarded 1 point. Each consecutive lap completed awarded 3 points. Bombs are the same shape and size as mystery blocks but are differentiated in colour and have a magnet in them. There is a correct orientation for the bomb to be considered upright. If a bomb is tipped over, it is triggered and the robot must reset. Each robot is also allowed to drop a banana during the race. A banana consists of a piece of paper of specified size which can contain a pattern or design which aims to confuse the other robot's navigation system. The robot with the most points at the end of each round is the winner.

Our robot design was optimized to drive fast and execute all functions (mystery block collection, bomb avoidance, etc) without reducing speed. It featured robot arms for block pickup, a printer-style banana release mechanism, a front wedge to constrain blocks and bombs, tape following capabilities, hall-effect sensor bomb detection, and home-made pendulum ramp detection.

### Block Collection System

I want to highlight the part of the robot I solely designed and manufactured: the robot arms.

The front of the robot was fitted with a wedge to funnel blocks towards the robot arms while preventing the blocks from tipping over. This allowed us to prevent bombs from detonating. We placed hall effect sensors within the wedge to detect if the block was a bomb. If it was a bomb, the robot arms would lift and allow the bomb to safely be swept to the side of the robot, undetonated. If it was not a bomb, the block would be caught by the robot arms.

<img width="578" height="448" alt="image" src="https://github.com/user-attachments/assets/fadc86ec-683c-4a49-917e-ed91314c3aed" />

<img width="976" height="549" alt="image" src="https://github.com/user-attachments/assets/83161702-d8e7-46ee-8ff6-8f1b8f988501" />

The above photo shows a CAD model of my robot arm design with a mystery block in the 'robot claw'.

This arm would be mounted onto the flat outcropping behind each front wheel in such a way as to allow the front wedge to funnel all blocks into the waiting claws. The blocks would then trigger a switch in the palm of the claw and the arm would grab the block, lift it up, and drop it into the collection area.

The claw in early testing:

<video controls width="600">
  <source src="/files/20230727_134713.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Skills developed:
circuit design, mechanical design, soldering, prototyping, debugging code, troubleshooting electrical issues, optimizing designs, integrating electromechanical systems.

Repairing the Robot Mid-Competition: \
<img width="481" height="478" alt="image" src="https://github.com/user-attachments/assets/d432042f-dcd0-4c03-ae84-aca1eedfe6d5" />

Being Interviewed by CTV News: \
![Screen_Recording_20230810_191053_Chrome](https://github.com/user-attachments/assets/e2619773-d4f2-45d4-92bd-24c657392d39)
...
