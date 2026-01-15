---
layout: single
title: Helmholtz Cage
permalink: /docs/projects/helmholtzcage/
sidebar:
  nav: "docs"
classes: wide
author_profile: true
---

I am leading a team of 5 BASc and BSC students to design and construct a 3 axis Helmholtz cage in order to cancel ambient magnetic fields and simulate dynamic in-orbit magnetic field conditions. This will enable UBC Orbit to perform magnetic testing of our cubesat ALEASAT and ensure that ALEASAT's dipole moment, as well as any magnetic field dependent and magnetic field generating components are performing within design and launch specifications.

As part of our design work, I used this [paper](https://www.sciencedirect.com/science/article/pii/S0307904X16303389) to develop a single axis (2 coils) static magnetic field simulation. The code for this simulation can be found [here](https://github.com/Casey-e-k/Helmholtz-Cage-Simulation/blob/main/Jupyter%20Notebook%20Helmholtz%20sim.ipynb). This simulation is being used by my team to test different system configurations and inform design decisions.

Example output:

<img width="639" height="601" alt="image" src="https://github.com/user-attachments/assets/b8ff4d8b-e80d-4f3c-b147-3b060a5c8706" />

<img width="612" height="495" alt="image" src="https://github.com/user-attachments/assets/84f52ed0-c501-4abc-9cc5-9da81e0a852b" />

Several design aspects are still in progress and we are waiting on specific information required to resolve these but the following imager is a general high level system design. Variable resistors will be placed in series with one coil in each axis in order to calibrate the resistances to achieve an equal current split. Each axis will be individually controlled.

<img width="648" height="564" alt="image" src="https://github.com/user-attachments/assets/b9446e06-84cd-4dd6-a9b4-808511eb84f4" />

prototype pair of coils:

<img width="619" height="548" alt="image" src="https://github.com/user-attachments/assets/adc9e92c-948b-4286-9a1c-5f39fabc8314" />

