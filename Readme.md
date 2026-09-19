# 🚗 Arduino Bluetooth Controlled RC Car 📶

This repository contains the Arduino code for a 4-wheel drive remote-controlled car. The car is controlled wirelessly via a smartphone using an HC-05 Bluetooth module and an Adafruit Motor Shield (L293D).

## 🛠️ Hardware Requirements
* Arduino Uno
* Adafruit L293D Motor Drive Shield (V1)
* HC-05 or HC-06 Bluetooth Module
* 4x BO Motors and Wheels
* 4WD Robot Chassis
* Battery/Power Supply (e.g., 2x 18650 Li-ion batteries)
* Jumper Wires

## 🔌 Circuit & Wiring Guide

**1. Bluetooth Module (HC-05) to Arduino:**
* **TX** Pin -> Arduino **Pin 9** (Software RX)
* **RX** Pin -> Arduino **Pin 10** (Software TX)
* **VCC** -> 5V
* **GND** -> GND

**2. Motors to L293D Shield:**
* Front-Left Motor -> **M1**
* Rear-Left Motor -> **M2**
* Front-Right Motor -> **M3**
* Rear-Right Motor -> **M4**

## 📚 Required Libraries
Before uploading the code, ensure you have installed the **Adafruit Motor Shield V1** library in your Arduino IDE.
* Go to `Sketch` -> `Include Library` -> `Manage Libraries`
* Search for `Adafruit Motor Shield` and install it.
* Alternatively, download it from [Adafruit's GitHub](https://learn.adafruit.com/adafruit-motor-shield/library-install).

## 📱 Smartphone Control Commands
Use any standard "Bluetooth RC Car" app from the Google Play Store. The app sends the following character commands to the Arduino:
* `F` : Move Forward
* `B` : Move Backward
* `L` : Turn Left
* `R` : Turn Right
* Any other character / Release button : Stop

## 🚀 How to Run
1. Assemble the hardware and complete the wiring.
2. **Important:** Disconnect the Bluetooth module's RX/TX pins or power while uploading the code to prevent serial conflicts.
3. Upload the `bluetooth_car.ino` file to your Arduino.
4. Reconnect the Bluetooth module.
5. Pair your phone with the HC-05 module (Default PIN is usually `0000` or `1234`).
6. Open your Bluetooth RC controller app, connect, and drive!

---
**Created by:** Shivshankar Kumar
