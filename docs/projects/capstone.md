---
layout: single
title: Ultrasonic Levitation
permalink: /docs/projects/capstone/
sidebar:
  nav: "docs"
classes: wide
author_profile: true
---
My Engineering Physics capstone project, spanning both the ENPH 459 and ENPH 479 capstone project courses, is the Ultrasonic Levitation project. The goal of this project is to produce holograms by using the interference patterns of phase shifted ultrasonic sound waves to levitate styrofoam beads and move them around.

We are continuing the work of a previous team in this project. They designed and fabricated a setup that was capable of levitating beads but not of producing holograms. The scope of future involves three main categories of activity:
1. Understanding the existing system implementation.
2. Characterizing the system.
3. Identifying and implementing upgrades to improve system performance so that we
can create holograms.

In ENPH 459 our main focus was on category 1. We split up the project into several areas of expertise, including hardware, code, and physics. My role was to gain a deep understanding of the physics.

In ENPH 479 we are moving into category 2. Our focus is to design a test campaign to dive deep into the system and determine the fundamental limiting factors that affect the strength of our acoustic traps and the maximum velocity and acceleration with which we can move the styrofoam beads. My role has involved hardware upgrades (particularly working with a teammate to build a new, more stable and versatile stand for our PCB). I am also responsible for writing python test code to facilitate the tests we have designed. The test code's job is to tell the transducer array what path we want the styrofoam bead to take. The test code will also aim to set up a foundation on which to build future bead control code when the time comes to implement code to rasterize an image in order to convert it to a holographic format.

### How it works

<img width="973" height="548" alt="image" src="https://github.com/user-attachments/assets/8fffe085-3fc1-4db3-8c02-c911abd3a422" />

For our purposes, a transducer is a small speaker that can emit an ultrasonic pressure wave (a sound wave). Our setup consists of an array of 256 transducers, of which we can control the relative phases of each sound wave emitted. This transducer array is placed above a reflective glass plate, with the transducers emitting toward the plate. By carefully choosing the relative phases (using a solver algorithm), we can control the pressure field inside the region of space between the transducer array and the reflective plate. This allows us to create a low pressure region, called a trap, which is capable of levitating a sufficiently small and lightweight particle, such as a styrofoam bead. By changing the relative phases accordingly, this trap can be moved around and the styrofoam bead will be moved around with it. If we can move the trap fast enough, we will experience an optical illusion called persistance of vision. This is a phenomenon that occurs because the human brain is limited in how fast it is capable of processing individual images. This happens because an image persists for a short time in the retina and neural pathways. If an object moves fast enough, individual successive instances of its position will appear to overlap and its motion will appeared blurred to us, much like how motion pictures were created.

<img width="886" height="476" alt="image" src="https://github.com/user-attachments/assets/d692579e-de3a-4624-8e63-32bbb4ae0242" />

visual demonstration of the wave interference concept I made using the manim animation library developed by Grant Sanderson for the 3Blue1Brown youtube channel:

<img src="/files/TransducerArrayScene@2025-03-25@06-05-42 (1).gif" width="600">

the traps occur at the vertical interfaces between yellow and blue regions in the heat map at the end of the video.

**disclaimer: the video above is NOT physically accurate, it is merely a qualitative visual to convey the general concept**

A real heat map for our system (created by a teammate):

<img width="753" height="594" alt="image" src="https://github.com/user-attachments/assets/b71614d5-f34b-492a-9c97-ca3822e9a81b" />





