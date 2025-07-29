# 🔥 AGNI 2.0.2.5 – Smart Fire Extinguisher Using ESP32

**AGNI 2025** is an autonomous smart fire extinguisher robot designed to identify and extinguish flames using an ESP32 microcontroller. It integrates sensors, motors, and a water-based extinguishing system to deliver fire safety solutions for confined areas like homes, labs, and server rooms.

---

## 🚀 Features

- 🔥 Real-time **fire detection** using an IR flame sensor  
- 🤖 Autonomous **navigation** toward the fire source  
- 💦 Smart **water pump activation** upon proximity to fire  
- 💡 Visual **LED indicator** when flame is detected  
- 📡 Optional **IoT monitoring** through Blynk or ThingSpeak  
- 🔋 Battery-powered mobility and portability  
- 🧠 Expandable with AI flame recognition or remote control

---

## 🧠 Components Used

| Component              | Quantity | Description                                 |
|------------------------|----------|---------------------------------------------|
| ESP32 Dev Board        | 1        | Brain of the robot, handles logic & control |
| IR Flame Sensor        | 1        | Detects presence of fire via infrared       |
| L298N Motor Driver     | 1        | Drives the motors based on ESP32 inputs     |
| DC Motors + Wheels     | 2        | Enables the robot to move                   |
| Water Pump + Tank      | 1        | Sprays water on the fire                    |
| LED Indicator          | 1        | Indicates detection status                  |
| Relay Module (Optional)| 1        | Controls water pump switching               |
| 18650 Battery / Power Bank | 1    | Supplies power to the system                |
| Chassis/Wheel Base     | 1        | Mounting frame for the robot                |
| Jumper Wires, Breadboard| -       | For connecting all components               |

---

## 🛠 Working Principle

1. The flame sensor constantly monitors for infrared signals that signify fire.
2. When fire is detected, ESP32 receives input and triggers motion:
   - Motor Driver (L298N) moves the robot toward the flame.
3. Upon nearing the flame (within range), the ESP32 activates a **water pump** via a relay.
4. Simultaneously, an LED blinks to indicate that a flame was detected and is being suppressed.
5. (Optional) Sensor data can be sent to a mobile dashboard using **Blynk** or **Thingspeak** for real-time monitoring.

---

## 🗺️ Circuit Connections

| Component        | ESP32 GPIO Pin |
|------------------|----------------|
| Flame Sensor     | GPIO 34        |
| LED              | GPIO 2         |
| Water Pump Relay | GPIO 13        |
| L298N Motor 1    | IN1, IN2 → GPIO 14, GPIO 27 |
| L298N Motor 2    | IN3, IN4 → GPIO 26, GPIO 25 |
| L298N ENA/ENB    | Connected to 5V |

---
