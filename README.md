#  Auto Power-Off System Using Sensor and Latching Circuit

##  Overview
This project demonstrates a **sensor-controlled latching system** with an **auto power-off** feature. The circuit uses both **analog and digital sensors** to decide whether the system should remain powered. If no sensor activity is detected, the system automatically shuts itself off using a transistor or relay circuit.

---

##  Features
-  **Latch mechanism** to keep the system powered after initial activation.
-  Monitors both **analog** (e.g., temperature, light) and **digital** (e.g., PIR, push button) sensors.
-  Automatically **turns off** the system when no input is detected.
-  **Blinking warning LED** before shutdown to alert the user.
-  **LED indicators** for active and idle status.

---

##  Components Used
| Component             | Function                                       |
|-----------------------|------------------------------------------------|
| Arduino Uno           | Main microcontroller                          |
| Analog Sensor (A0)    | E.g., potentiometer or TMP36                  |
| Digital Sensor (D2)   | E.g., PIR motion sensor or push button        |
| NPN Transistor / Relay| Controls system power                         |
| LED (D10)             | Indicates system is active                    |
| LED (D11)             | Blinks before shutdown                        |
| Resistors             | For LEDs and sensors                          |
| Breadboard + Wires    | Circuit building                              |

---

##  System Logic
1. **Startup**: The relay/transistor is initially ON to power the system.
2. **Sensor Monitoring**:
   - If **analog > 200** OR **digital sensor = HIGH**, the system remains active.
   - If no sensor input is detected, the system enters **idle mode**.
3. **Auto Shutdown**:
   - The **idle LED blinks 5 times**, then power is shut off by disabling the relay/transistor.

---
