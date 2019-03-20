---
layout: post
title:  "Coding like Curiosity: Introduction"
date:   2013-12-17
---

![image](/assets/mars_rover.jpg)
*Curiosity Mars Rover - Right Side View (Photo credit: Wikipedia)*

Real-time operating systems have fascinated me since before I even knew what they were. The first real-time application that really made me stop and think was the Curiosity’s (or Mars Science Laboratory’s) software platform. One set of applications are responsible for controlling everything the rover can accomplish. This huge amount of responsibility is handled by a strictly scheduled operating system called a real-time operating system (RTOS). To learn more about how to create critical software for these types of systems, I have decided to adopt some of the software architectural principles, as described by Ben Cichy [0], in a much (MUCH) smaller rover project of my own.

I am going to create a software platform for an Arduino powered robot that will run on an RTOS and be separated into independent modules just like the Curiosity flight software. It will communicate with my laptop wirelessly to provide log details and accept basic commands. The robot itself will be almost entirely autonomous, utilizing an infrared sensor array to detect platform edges and another pair of infrared detectors to avoid obstacles. I’ll be using the Arduino Uno and only have about 32KB for the entire software, including the RTOS libraries. As such, I plan to use the nilRTOS (now named ChNil) [1] libraries, which were derived from the ChibiOS and are extremely small and lightweight.

This blog will be updated as the project progresses. I hope to have it all completed by May 2014. I’ll update with a parts list in the next segment in case any one would like to try a project of their own.

       0: Cichy, B. (2010). The Evolution of the Mars Science Laboratory Flight Software. 2010 Workshop on Spacecraft Flight Software. Lecture conducted from California Institute of Technology. Pasadena, CA

       1: https://github.com/greiman/ChNil
