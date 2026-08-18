# DC-DC-open-loop-Buck-convertor
# 🔋 Closed-Loop Buck Converter

A **Closed-Loop Buck Converter** designed to step down a higher DC input voltage to a regulated lower DC output voltage using PWM-based switching and feedback control.

## 📌 Overview

A buck converter is a DC-DC converter used to reduce voltage efficiently.

In this project, a **closed-loop approach** is used to improve output voltage stability. The output is monitored and the switching operation is controlled to maintain the desired voltage under varying conditions.

## ⚙️ Working Principle

The **NE555 timer** generates the PWM signal, while the switching stage controls the energy transferred through the inductor. The capacitor filters the output to obtain a smoother DC voltage.

```text
DC Input
   ↓
NE555 Timer
   ↓
PWM Generation
   ↓
MOSFET Switching
   ↓
Inductor
   ↓
Output Filtering
   ↓
DC Output
```

## 🔧 Components

* NE555 Timer IC
* MOSFET
* 100 µH Inductor
* 100 µF Capacitor
* 10 µF Capacitor
* 0.01 µF Capacitor
* 10 kΩ Potentiometer
* Resistors
* Breadboard
* Universal PCB
* Jumper Wires

## 📐 Circuit Diagram

![Circuit Diagram](<img width="1920" height="1140" alt="Screenshot 2026-03-26 152433" src="https://github.com/user-attachments/assets/b1a8650e-5689-43e7-ad78-fb6d866c3c1c" />
.jpg)



## 🔩 Physical Circuit

![Breadboard Circuit](<img width="1040" height="646" alt="WhatsApp Image 2026-04-23 at 9 31 13 PM (1)" src="https://github.com/user-attachments/assets/38121263-3218-49ab-84ee-78e2fd0ea7cf" />
.jpg)



## 🛠️ Key Concepts

* DC-DC Conversion
* Buck Converter
* PWM
* MOSFET Switching
* Feedback Control
* Voltage Regulation
* Power Electronics
