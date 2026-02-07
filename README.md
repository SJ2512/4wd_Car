# Autonomous Mobile Robot Platform (V1–V3 Evolution)

## Overview

This project represents the first complete robotics system I built and the starting point of my work in embedded systems and mechatronics.

Developed across multiple iterations, the platform evolved from a basic obstacle-avoidance robot into a multi-controller semi-autonomous mobile system with manual control, sensor upgrades, and improved power architecture.

Rather than a single build, this project reflects an **engineering progression across three versions**, each solving limitations of the previous design.

It served as the foundation for all later robotics and mechatronics projects.

---

# Why this project exists

This was my first serious electronics and robotics system built after entering the mechatronics field.

The goal was to:

* Understand embedded control systems
* Learn power distribution in mobile robots
* Integrate sensors with real-time control
* Explore autonomous vs manual control
* Develop system planning and debugging discipline

The project became a long-term learning platform rather than a one-time build.

---

# Version Evolution

## Version 1 — Basic Autonomous Obstacle Avoidance

Initial prototype built using Arduino Uno.

### Features

* Ultrasonic-based obstacle detection
* Servo-mounted scanning sensor
* Basic autonomous navigation
* Differential drive chassis

### Hardware
check V1/Readme.md

### Key Outcome

Validated basic autonomous navigation and sensor-based motion control.

Also exposed early issues with:

* voltage drops
* wiring planning
* component quality

---

## Version 2 — Manual Control & Connectivity Upgrade

Second iteration introduced remote control and communication capability.

### Upgrades

* Bluetooth manual control
* ESP32 integration (replacing external Bluetooth module)
* Web-based control interface
* Data logging via ESP32 web server

### Learning Focus

* Wireless control systems
* Serial communication
* Real-time command handling
* Embedded networking basics

This version transitioned the robot from purely autonomous to hybrid manual platform.

---

## Version 3 — Dual-Mode Semi-Autonomous Platform

Final and most advanced iteration.

### Major Upgrades

* Master–slave architecture

  * ESP32 (master)
  * Arduino Mega (slave control)
* Dual operation modes:

  * Manual control
  * Autonomous navigation
* ToF sensor replacing ultrasonic for improved accuracy
* MPU6050 for orientation and yaw tracking
* BTS7960 high-current motor drivers
* Upgraded 12V motors
* Logic level converters
* 4S Li-ion battery system
* Dedicated buck converters for stable rails

### Result

A significantly more stable and capable mobile robot capable of both manual and sensor-driven operation.

---

# System Architecture (Final Version)

## Control

* ESP32 master controller
* Arduino Mega slave for motion & sensors
* UART communication between controllers

## Sensors

* ToF distance sensor
* MPU6050 orientation tracking

## Drive System

* 12V DC motors
* BTS7960 high-current drivers

## Power

* 4S Li-ion battery
* Multi-rail buck converters
* Dedicated logic and motor supply separation

---

# Engineering Challenges Faced

### Power Instability

Early versions suffered from voltage drop and unreliable operation.
Solved by introducing:

* Proper buck regulation
* Power rail separation
* Higher quality batteries

### Wiring Complexity

As system scaled:

* Wiring became dense
* Chassis space reduced

Solved using:

* Hex spacers
* Layered mounting
* Structured routing

### Component Selection

Cheap components caused:

* inconsistent performance
* debugging difficulty

Later versions used:

* higher current drivers
* better sensors
* proper voltage regulation

---

# Key Engineering Lessons

* Power distribution determines system stability
* Planning wiring and layout early prevents major redesign
* Component interaction matters more than individual specs
* Always prototype architecture before full integration
* System evolution is more valuable than single builds

This project shaped the design philosophy used in all later robotics systems.

---

# Current Status

Completed as a learning and development platform.
Serves as the foundational project for later work in:

* mobile robotics
* manipulators
* multi-controller systems

