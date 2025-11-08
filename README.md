# 🛰️ In-Space CanSat 2024–25 Structural Design

This repository contains the detailed CAD model and manufacturing details of our **In-Space CanSat 2024–25** — a compact satellite prototype designed for high-altitude missions and recovery using autonomous systems.  

Below is a breakdown of each **structural compartment** and its functionality, referencing both the CAD design and the manufactured model.

---

## 🧩 Structural Overview

| Component | Function | Material |
|------------|-----------|-----------|
| Main Parachute Compartment | Houses main parachute and release servos | PLA+ |
| Main Parachute Lid | Lid tied to drogue chute; servo-controlled release | PLA+ |
| Carbon Fiber Rods | Structural frame alignment | Carbon Fiber (Ø4mm) |
| Clamps | Lock each module on rods | PLA+ |
| PCB Plate | Holds sensors and main PCB | FR4 / PLA+ Mount |
| Emergency Compartment | Houses emergency parachute & release system | PLA+ |
| Emergency Door | Rotating door for emergency parachute | PLA+ |
| Gyro Assembly | Attitude control & stabilization | PLA+ + BLDC + Servos |
| Battery Compartment | Power distribution system housing | PLA+ |

---

## 🪂 1. Main Parachute Compartment
The **topmost compartment** securely houses the **main parachute**, which is also tied to this module.  
It integrates **two servo motors** responsible for releasing the parachute lid upon reaching a specific altitude.

- Contains: Main parachute (folded), 2× release servos  
- Function: Controlled deployment of the main parachute  
- Location: Topmost cylindrical section  
- Material: PLA+  
- Mounting: Fixed on carbon fiber rods with clamps  

---

## 🧢 2. Main Parachute Lid
Positioned above the main parachute compartment, the **lid** is connected to the **drogue parachute** and held in place by two servos.  
When the system detects the target altitude, the servos rotate to release the lid, triggering the main parachute deployment sequence.

- Mechanism: Dual-servo release  
- Connection: Tied with drogue parachute  
- Function: Seals main chute compartment until release  
- Material: PLA+  

---

## 🦾 3. Carbon Fiber Rods
The structure is reinforced using **four 4mm carbon fiber rods** that extend through all compartments.  
These rods ensure **vertical alignment, strength, and stability**, providing a rigid cylindrical frame.

- Quantity: 4 rods  
- Diameter: 4 mm  
- Purpose: Structural alignment and load-bearing  
- Material: Carbon Fiber  

---

## 🔩 4. Clamps
The **red clamps** are used to lock each compartment onto the carbon fiber rods.  
They are fastened using **M2 screws and nuts**, ensuring secure attachment and easy modular disassembly.

- Color: Red  
- Material: PLA+  
- Fasteners: M2 screws and nuts  
- Function: Structural locking and height adjustment  

---

## 🧠 5. PCB Plate
Mounted just below the parachute compartment, this **plate** acts as the main electronics deck.  
All the **sensors, microcontrollers, and communication modules** are attached here.

- Components Mounted: Sensors, microcontrollers, telemetry units  
- Material: FR4 or PLA+ base plate  
- Role: Electrical & sensor hub  
- Function: Integrates flight data processing and control logic  

---

## 🚨 6. Emergency Compartment
This compartment ensures **redundant safety** in case the main parachute fails to deploy.  
It houses the **emergency parachute**, a **servo-operated release door**, and a **spring-loaded mechanism** to eject the parachute.

- Components: Emergency chute, spring plate, servo motor  
- Function: Deploys backup parachute during main chute failure  
- Mechanism: Servo rotation releases spring-tensioned door  
- Material: PLA+  

---

## 🌀 7. Emergency Door
The **emergency door** seals the emergency compartment and holds the parachute in place.  
During an emergency trigger, the servo rotates the door, releasing the parachute outward.

- Type: Rotating latch door  
- Mechanism: Servo rotation-based  
- Function: Opens for emergency parachute ejection  
- Material: PLA+  

---

## ⚙️ 8. Gyro Assembly
The **gyro system** is an active stabilization module consisting of:
- **Outer ring**,  
- **Inner ring**,  
- **BLDC holder**, and  
- **Flywheel**.

It includes **2 servo motors** and **1 BLDC motor**:
- The **inner ring** is rotated by one servo mounted in the **outer ring**.
- The **second servo** rotates the **BLDC holder**, changing the flywheel axis.
- The **flywheel**, attached to the **BLDC motor**, provides stabilization via gyroscopic precession.

- Components: Outer ring, inner ring, BLDC holder, flywheel  
- Motors: 2× servos, 1× BLDC  
- Function: Attitude stabilization and orientation control  
- Material: PLA+ and metal components  

---

## 🔋 9. Battery Compartment
The **battery compartment** is located at the bottom and houses the **battery pack** and **power distribution system**.  
It supplies power to all electronics, including the servos, BLDC motor, sensors, and control units.

- Components: Battery pack, wiring, connectors, distribution board  
- Function: Centralized power management  
- Output: Regulated supply to sensors, servos, and controllers  
- Material: PLA+  

---

## 🧱 Assembly Summary

- **Material:** PLA+ (3D printed) and Carbon Fiber rods  
- **Fasteners:** M2 screws and nuts  
- **Alignment:** Modular cylindrical frame  
- **Design Software:** SolidWorks 2022 SP1.0  
- **Manufacturing Method:** FDM 3D Printing  

---

## 📸 Gallery

<div align="center">

### 🧱 CAD Model
<img width="384" height="715" alt="Screenshot 2025-11-08 211547" src="https://github.com/user-attachments/assets/e25a2ada-2a14-4155-965d-6850096d2d3e" />


---

### 🛰️ Real Manufactured Model
![WhatsApp Image 2025-11-08 at 22 26 55_d042e1ac](https://github.com/user-attachments/assets/09fa0145-0a65-4742-b035-2e6ac998c071)


</div>


## 🧩 Key Highlights
- Modular, serviceable, and lightweight design  
- Dual redundancy in parachute deployment  
- Active stabilization via gyro system  
- Robust PLA+ and carbon fiber structure  
- Fully 3D-printed mechanical design  

---

> **Developed by:** *Team In-Space CanSat 2024–25*  
> **Design & Simulation:** SolidWorks 2022  
> **Material Used:** PLA+ and Carbon Fiber  
> **Mission Type:** High-altitude data acquisition and autonomous recovery  
> **Category:** CanSat Structural System Design  
