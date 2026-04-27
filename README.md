# 🏎️ ESP8266 Wi-Fi Robot Controller

An interactive, browser-based RC car project utilizing the ESP8266 as a Web Server and Access Point. This project provides a smooth "touch-and-go" interface for real-time motor control and speed adjustment.

## 🚀 Key Features
- **App-Free Control:** No mobile app required; operates via any modern web browser.
- **Dynamic Speed Control:** Real-time PWM speed adjustment (0–1023) via a slider.
- **Responsive UI:** Supports both mouse clicks (PC) and touch events (Mobile).
- **Standalone Network:** Creates its own Wi-Fi hotspot (**Robot_Car**).

## 🛠️ Hardware Requirements
- **Microcontroller:** ESP8266 (NodeMCU or D1 Mini)
- **Motor Driver:** L298N Dual H-Bridge
- **Motors:** 2x DC Gear Motors
- **Power:** 2x 18650 Li-ion Batteries (7.4V)
- **Chassis:** 2WD/4WD Robot Kit

## 🔌 Wiring Diagram (L298N to ESP8266)

| L298N Pin | NodeMCU Pin | GPIO | Function |
| :--- | :--- | :--- | :--- |
| **ENA** | D5 | GPIO14 | Left Motor Speed (PWM) |
| **IN1** | D1 | GPIO5  | Left Motor Direction |
| **IN2** | D2 | GPIO4  | Left Motor Direction |
| **IN3** | D4 | GPIO2  | Right Motor Direction |
| **IN4** | D7 | GPIO13 | Right Motor Direction |
| **ENB** | D6 | GPIO12 | Right Motor Speed (PWM) |

## 🕹️ Setup Instructions
1. **Flash Code:** Upload the `.ino` file to your ESP8266 using the Arduino IDE.
2. **Connect:** Scan for Wi-Fi on your phone and connect to `Robot_Car` (Password: `Via12345`).
3. **Control:** Open your browser and navigate to `http://192.168.4.1`.
4. **Calibrate:** Use the slider to find the minimum starting torque for your motors.

## ⚠️ Safety Note
Ensure the battery ground is connected to **both** the L298N GND and the ESP8266 GND for a common reference point.
