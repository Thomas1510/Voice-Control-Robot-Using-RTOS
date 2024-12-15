# Voice and Bluetooth Controlled Robot with Obstacle Avoidance (RTOS-Based)

This repository contains the code for a multifunctional robotic system capable of being controlled via Bluetooth and voice commands. It integrates advanced obstacle avoidance using an ultrasonic sensor and servo motor. Additionally, the robot's functionality is enhanced by using an **RTOS (Real-Time Operating System)** to ensure efficient task management and real-time responsiveness.

## Features

### 1. Bluetooth Control
- Control the robot's movement with simple Bluetooth commands:
  - `F`: Move Forward
  - `B`: Move Backward
  - `L`: Turn Left
  - `R`: Turn Right
  - `S`: Stop

### 2. Voice Control
- Operate the robot with voice commands mapped to specific actions:
  - `^`: Move Forward
  - `-`: Move Backward
  - `<`: Turn Left (only if the path is clear)
  - `>`: Turn Right (only if the path is clear)
  - `*`: Stop

### 3. Obstacle Avoidance
- Automatic detection of obstacles using an ultrasonic sensor.
- The robot evaluates left and right paths and chooses the safest direction when an obstacle is detected within 12 cm.

### 4. Servo-Based Scanning
- The ultrasonic sensor, mounted on a servo motor, scans left and right to detect obstacles during obstacle avoidance.

### 5. Motor Control
- Uses the Adafruit Motor Shield to control four DC motors for precise movements.

### 6. Real-Time Distance Measurement
- Ultrasonic sensor calculates and provides real-time distance from obstacles.

### 7. RTOS-Based Architecture
- The robot utilizes **RTOS** for:
  - Scheduling tasks such as Bluetooth control, voice command processing, and obstacle avoidance.
  - Ensuring real-time responsiveness for critical tasks like distance measurement and movement decisions.
  - Efficient resource utilization for simultaneous control and monitoring.

## Components Used
- **Arduino Uno** (or compatible microcontroller)
- **Adafruit Motor Shield**
- **4 DC Motors**
- **Ultrasonic Sensor** (HC-SR04)
- **Servo Motor**
- **Bluetooth Module** (e.g., HC-05/HC-06)

## How to Use
1. **Setup**: Connect the components as per the circuit design and upload the code to the Arduino.
2. **Control**: Use a Bluetooth terminal app or voice commands to control the robot.
3. **Obstacle Avoidance**: Watch the robot automatically avoid obstacles when in operation.

## Circuit Diagram
Include your circuit diagram or description here.

## RTOS Integration
The code is structured to use an **RTOS** for:
- Task prioritization: Critical tasks like obstacle avoidance have higher priority.
- Multitasking: Concurrent execution of Bluetooth and voice control tasks.
- Improved efficiency: Ensures seamless operation without delays or resource conflicts.

### Example Tasks in RTOS:
- **Task 1**: Bluetooth command listener.
- **Task 2**: Voice command processor.
- **Task 3**: Obstacle detection and decision-making.
- **Task 4**: Motor control for movement execution.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/robot-control.git
