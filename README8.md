
# 🔥 IoT Based Fire Department Alerting System

## 📌 Project Overview

The **IoT Based Fire Department Alerting System** is a smart safety system designed to detect fire incidents automatically and send instant alerts to the fire department or responsible authority.

This system uses sensors to monitor environmental conditions like temperature and smoke level. When a fire is detected, the IoT device processes the data and sends an emergency notification through the internet.

The main goal of this project is to reduce fire response time and minimize damage by providing an automatic alert mechanism.

---

## 🎯 Objectives

- Detect fire automatically using sensors
- Monitor temperature and smoke levels
- Send instant fire alerts remotely
- Reduce human response delay
- Improve safety in homes, offices, and industries

---

## 🛠️ Hardware Components

| Component | Description |
|---|---|
| ESP32 / NodeMCU | Main IoT controller |
| Flame Sensor | Detects fire/flame |
| MQ-2 Smoke Sensor | Detects smoke/gas |
| Temperature Sensor (DHT11/LM35) | Measures temperature |
| Buzzer | Local fire alarm |
| LED | Warning indicator |
| GSM Module / WiFi | Sends alert message |
| Relay Module (Optional) | Controls external devices |
| Battery/Power Supply | Power source |

---

## 💻 Software Requirements

- Arduino IDE
- Embedded C/C++
- ESP32 Board Package
- IoT Cloud Platform (Optional)
- Blynk / Firebase / MQTT (Optional)

---

## ⚙️ Working Principle

1. Sensors continuously monitor the environment.
2. Flame sensor detects fire presence.
3. Smoke sensor checks smoke intensity.
4. Temperature sensor monitors heat level.
5. ESP32 collects sensor data.
6. If fire conditions are detected:
   - Buzzer turns ON
   - LED warning starts
   - Alert message is sent through internet/GSM
7. Fire department or user receives the emergency notification.

---

## 🔄 System Flow
