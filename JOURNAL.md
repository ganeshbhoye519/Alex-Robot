---
title: "Alex"
author: "Ganesh"
description: "Autonomous tracked companion rover"
created_at: "2024-10-011"
---

* **What I did:** Finalized the system architecture, component functions, development milestones, and budget estimation for Pragya.

### System Functions

**🔹 Movement Functions**
* Tank-style movement (tracked chassis) → fast & powerful on land.
* Maze solving → detects paths, avoids dead-ends, finds exit.
* Line following → IR sensors keep robot on black/white lines.
* Object following → follows a person or moving target.

**🔹 Vision & AI Functions**
* Face detection / recognition (via Pi Camera + Raspberry Pi).
* Object color detection → e.g., detect red or green cube.
* Object sorting with arm → pick up cube with servo gripper, place in correct spot.
* Eye display (small TFT screen) → shows robot’s mood (happy/angry/sleepy eyes).

**🔹 Interaction Functions**
* Voice talking (speaker) → robot can greet, answer basic questions.
* Voice listening (mic) → robot understands commands (“go left,” “pick cube,” etc.).
* Conversation with sir/ma’am → AI-powered Q&A (using Raspberry Pi).

**🔹 Control & Safety**
* Ultrasonic sensors → avoid collisions with walls/objects.
* IMU (gyroscope/accelerometer) → keeps balance, helps navigation.
* Battery + UBEC → safe power for Pi + motors + servos.
* Arduino Uno → handles motors/servos smoothly, while Pi does AI.

---

### Development Milestones

* **Milestone 1: Setup & Base Movement**
  * Install Raspberry Pi OS, test HDMI/SSH/VNC access.
  * Connect Raspberry Pi ↔ Arduino Nano (USB/serial).
  * Assemble tank chassis (3D print parts, mount DC motors + driver).
  * Control robot movement with Pi sending commands → Arduino.
  * ✅ **Output:** Tank robot moves with Pi as brain + Arduino as muscle.

* **Milestone 2: Sensors Integration (Basic)**
  * Add Ultrasonic sensor + IR line sensors.
  * Arduino reads sensor data, sends info to Raspberry Pi.
  * Pi processes and decides actions.
  * ✅ **Output:** Pi makes robot follow lines & avoid obstacles.

* **Milestone 3: Arm & Servo (Early AI)**
  * 3D print robotic arm + gripper.
  * Control servos via Arduino, but Pi decides when to pick/place.
  * ✅ **Output:** Robot can grab/release objects under Pi’s command.

* **Milestone 4: Pi Camera + TFT Display**
  * Mount Pi Camera.
  * Show live feed on Pi or process with OpenCV.
  * Add TFT display for robot eyes/moods.
  * ✅ **Output:** Robot has “eyes” & vision activated.

* **Milestone 5: AI Functions**
  * Face detection & recognition on Pi.
  * Voice assistant setup (speech-to-text + text-to-speech).
  * Display eyes reacting to events.
  * ✅ **Output:** Robot can see faces, talk, and show expressions.

* **Milestone 6: Object Intelligence**
  * Color detection (red/green cubes).
  * Pi sends cube info → Arduino moves arm to sort cubes.
  * Object following with Pi camera.
  * ✅ **Output:** Robot sorts cubes + follows moving objects.

* **Milestone 7: Final Integration**
  * Combine tank movement, sensors, arm, AI.
  * Full maze solving + talking + object sorting together.
  * ✅ **Output:** A smooth, multitask robot with Pi + Arduino working together.

---

**Total time spent: 49h**
