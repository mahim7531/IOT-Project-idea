
# 🌊 IoT Flood Monitoring & Alerting System

## 📌 Project Overview

The **IoT Flood Monitoring & Alerting System** is a smart environmental monitoring system designed to detect rising water levels and provide early flood warnings.

This system uses IoT sensors to monitor water level, rainfall, and environmental conditions. When the water level reaches a critical point, the system automatically sends alerts to users or authorities through internet-based communication.

The main purpose of this project is to provide an early warning system to reduce flood damage and protect lives and properties.

---

## 🎯 Objectives

- Monitor water level in real-time
- Detect possible flood situations early
- Send automatic emergency alerts
- Reduce human response time
- Provide a low-cost flood monitoring solution

---

## 🛠️ Hardware Components

| Component | Description |
|---|---|
| ESP32 / NodeMCU | Main IoT controller |
| Water Level Sensor | Measures water level |
| Ultrasonic Sensor (HC-SR04) | Detects water height |
| Rain Sensor | Detects rainfall |
| Temperature Sensor (DHT11) | Monitors environment |
| Buzzer | Emergency alarm |
| LED | Warning indicator |
| GSM Module / WiFi | Communication system |
| OLED Display (Optional) | Shows sensor data |
| Battery / Power Supply | Power source |

---

## 💻 Software Requirements

- Arduino IDE
- Embedded C/C++
- ESP32 Board Package
- IoT Platform (Optional)

Possible Platforms:
- Blynk
- Firebase
- ThingSpeak
- MQTT

---

## ⚙️ Working Principle

1. Sensors continuously monitor water level and rainfall.
2. ESP32 collects sensor data.
3. The system compares collected data with predefined danger levels.
4. If water level increases above the safe limit:
   - Buzzer turns ON
   - Warning LED starts blinking
   - Alert notification is sent
5. Users or authorities receive flood warnings instantly.

---

## 🔄 System Flow
