# In-Space-CANSAT-Design
# 🛰️ CanSat Parachute Release Mechanism using Servo

This project demonstrates a **servo-based parachute release mechanism** designed for **CanSat** missions.  
The goal is to **safely deploy a parachute** at a specific altitude or event trigger, ensuring a controlled descent and safe landing of the CanSat payload.

---

## 🚀 Overview

During a CanSat mission, after launch and separation, the satellite must descend slowly using a parachute.  
This system uses a **servo motor** controlled by a microcontroller (like Arduino) to **release the parachute** at a specific trigger condition — such as reaching a target altitude or receiving a command from the onboard system.

---

## ⚙️ System Components

| Component | Description |
|------------|-------------|
| **Microcontroller** | Arduino Nano / Uno / ATmega328P (controls the servo) |
| **Servo Motor** | Micro servo (SG90 or MG90S) for mechanical release |
| **Trigger Sensor** | Barometric sensor (e.g., BMP180 / BMP280) or any other trigger condition |
| **Power Supply** | Li-ion / LiPo battery (5V regulated) |
| **Parachute Bay Lock** | Simple mechanical latch or pin mechanism held by the servo arm |

---

## 🧠 Working Principle

1. The CanSat is launched with the parachute compartment **locked** by the servo arm.  
2. The microcontroller continuously **monitors altitude** or waits for a release signal.  
3. When the **trigger condition** is met (e.g., below a certain altitude or timer expired):  
   - The servo rotates to **unlock** the mechanism.  
   - The parachute **deploys automatically** due to internal spring or air pressure.  
4. After release, the CanSat **descends safely** under the parachute.

---

## 🔩 Circuit Diagram

- **Servo signal pin** → Arduino digital pin (e.g., D9)  
- **Servo VCC** → 5V  
- **Servo GND** → GND  
- **Sensor (optional)** → Connected via I2C (SDA/SCL)  
- **Battery** → 5V regulated input to Arduino VIN or 5V pin

> ⚠️ Always use a separate power source for the servo if it draws high current.

---

## 💻 Example Arduino Code

```cpp
#include <Servo.h>
Servo chuteServo;

int releaseAltitude = 200;  // meters
bool released = false;

void setup() {
  chuteServo.attach(9);
  chuteServo.write(0); // Locked position
  Serial.begin(9600);
}

void loop() {
  int currentAltitude = readAltitude(); // Replace with actual sensor reading

  if (currentAltitude <= releaseAltitude && !released) {
    chuteServo.write(90); // Unlock
    Serial.println("Parachute Released!");
    released = true;
  }
}

int readAltitude() {
  // Dummy altitude simulation
  static int alt = 1000;
  alt -= 10;
  delay(100);
  return alt;
}
