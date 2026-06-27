# 🗑️ ESP32 IoT Smart Dustbin

An IoT-based smart dustbin system using ESP32 that automatically opens the lid, monitors waste level, and provides real-time status updates.

## 📌 Project Overview

The ESP32 IoT Smart Dustbin is an automated waste management system designed to improve hygiene and smart waste monitoring.

The system uses an ultrasonic sensor to measure the waste level and a servo motor to automatically open/close the dustbin lid when a person comes near.

## 🚀 Features

- ✅ Automatic lid opening system
- ✅ Waste level monitoring
- ✅ ESP32 WiFi connectivity
- ✅ Real-time IoT dashboard support
- ✅ Full dustbin alert system
- ✅ Low-cost hardware implementation
- ✅ Easy to build and modify

## 🛠️ Hardware Components

| Component | Quantity |
|-----------|----------|
| ESP32 Development Board | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| SG90 Servo Motor | 1 |
| Buzzer | 1 |
| LED | 1 |
| Breadboard | 1 |
| Jumper Wires | Required |
| Power Supply | 1 |

## 🔌 Circuit Connection

### Ultrasonic Sensor (HC-SR04)

| Sensor Pin | ESP32 Pin |
|------------|-----------|
| VCC | 5V |
| GND | GND |
| TRIG | GPIO 5 |
| ECHO | GPIO 18 |


### Servo Motor

| Servo Pin | ESP32 Pin |
|-----------|-----------|
| VCC | 5V |
| GND | GND |
| Signal | GPIO 13 |


### Buzzer

| Buzzer Pin | ESP32 Pin |
|------------|-----------|
| Positive | GPIO 12 |
| Negative | GND |

## ⚙️ Working Principle

1. Ultrasonic sensor detects the distance of the user.
2. If a person comes near the dustbin:
   - Servo motor rotates.
   - Lid opens automatically.
3. After a few seconds:
   - Lid closes automatically.
4. Ultrasonic sensor measures garbage level.
5. When the dustbin becomes full:
   - Buzzer gives an alert.
   - IoT dashboard shows the status.

## 💻 Software Requirements

- Arduino IDE
- ESP32 Board Package
- Blynk IoT Platform

## 📚 Libraries Used
