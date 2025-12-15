# Ultrasonic Distance Measurement System (Arduino UNO)

![Arduino](https://img.shields.io/badge/Arduino-UNO-blue)
![Language](https://img.shields.io/badge/Language-C%2B%2B-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Embedded%20Systems-orange)
![Status](https://img.shields.io/badge/Status-Stable-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Project Overview

> **Portfolio-grade embedded systems project demonstrating ultrasonic sensing, real-time signal processing, and hardware–software integration using Arduino UNO.**

This project implements a distance measurement system using an **HC-SR04 ultrasonic sensor** and an **Arduino UNO**, with visual feedback through an LED. It continuously calculates object distance and triggers output based on defined thresholds.

This project is intentionally simple, deterministic, and readable — optimized for **academics, interviews, and embedded systems fundamentals**.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Hardware Requirements

### Components
- Arduino UNO
- HC-SR04 Ultrasonic Sensor
- LED (any color)
- 220Ω resistor
- Jumper wires (male–male)
- Breadboard (optional)
- USB Type-B cable

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Circuit Connections

### HC-SR04 → Arduino UNO

| HC-SR04 Pin | Arduino Pin |
|------------|------------|
| VCC        | 5V         |
| GND        | GND        |
| TRIG       | D9         |
| ECHO       | D10        |

### LED
- Anode (+) → D3 (via 220Ω resistor)
- Cathode (–) → GND

📌 **Circuit Diagram**  
- in circuit_diagram.png

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Working Principle

1. Arduino sends a **10µs trigger pulse** to the sensor.
2. HC-SR04 emits ultrasonic waves (40 kHz).
3. Waves reflect from the object and return.
4. Echo pulse duration is measured.
5. Distance is calculated using:
   -  Distance (cm) = (Duration × 0.0343) / 2
6. LED turns ON when the distance meets the threshold condition.

   
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Software Requirements

- Arduino IDE (latest version)
- Board: Arduino UNO
- Baud Rate: 9600
- No external libraries required

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ultrasonic-distance-arduino.git
2. Open arduino_sketch.ino in Arduino IDE.
3. Connect Arduino UNO via USB.
4. Select:
      -  Board → Arduino UNO
      -  Port → Correct COM/USB port
      -  Upload the code.
      -  Open Serial Monitor (9600 baud).
      -  Move an object in front of the sensor and observe behavior.
  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Learning Outcomes

    - Ultrasonic time-of-flight measurement
    - GPIO and digital signal handling
    - Sensor-to-actuator logic design
    - Writing clean embedded C++ code
    - Hardware–software integration fundamentals

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Use Cases

    - Obstacle detection
    - Parking assistance prototype
    - Robotics distance sensing
    - Smart automation demos
    - Embedded systems practicals
