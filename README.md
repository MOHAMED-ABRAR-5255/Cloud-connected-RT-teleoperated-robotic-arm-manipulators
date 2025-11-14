# ESP8266 → STM32F103RB Servo Control (UART Based Web Control)

This project allows you to control a **servo motor** connected to an **STM32F103RB** using a **web interface hosted by an ESP8266**.  
The ESP8266 creates a simple HTTP server and sends servo angle commands to the STM32 via **UART communication**.

---

## Features

- ESP8266 hosts a local webserver (Station Mode + AP Fallback)
- UI with real-time slider to set servo angle (0°–180°)
- ESP8266 sends commands over UART
- STM32 reads serial command, parses angle, and drives servo using PWM
- Safe and stable wiring (common GND, external power for servo)

---

## 🧩 Hardware Used

- **STM32F103RB / Blue Pill**
- **ESP8266 NodeMCU (Recommended)**
- **SG90 / MG996R Servo**
- **External 5V Power Supply (for servo)**
- **Jumper wires**

---

## 📡 ESP8266 Code (Webserver)

The ESP8266 hosts a simple webpage.  

👉 Full code inside WebServer.ino

---

## ⚙ STM32 Code (Servo Control)

The STM32 receives UART commands and sends signals to the arm.

👉 Full code inside stm.ino

---

## 📡 ESP32 cam Code (Webserver)

The ESP32-cam code hosts a simple webpage with the camera feed.

👉 Full code inside esp_cam.ino
