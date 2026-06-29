# 🌦️ IoT Weather Reporting System

## 📌 Project Overview

The **IoT Weather Reporting System** is a smart weather monitoring project that collects real-time environmental data and uploads it to an online platform using IoT technology.

The system uses different sensors to measure temperature, humidity, and rainfall conditions. An IoT microcontroller collects the sensor data, processes it, and sends the information to a web server/cloud platform through a WiFi connection.

Users can monitor live weather conditions remotely and receive alerts when weather parameters cross predefined limits.

---

## 🎯 Objectives

- Monitor real-time weather conditions
- Measure temperature and humidity
- Detect rainfall status
- Send weather data through the internet
- Provide remote weather monitoring
- Generate alerts during critical conditions

---

## 🛠️ Hardware Components

| Component | Description |
|---|---|
| ESP32 / ESP8266 | IoT Controller with WiFi |
| DHT11 / DHT22 Sensor | Temperature & Humidity Measurement |
| Rain Drop Sensor | Rain Detection |
| OLED/LCD Display | Display Weather Data |
| Buzzer | Alert System |
| LED | Status Indicator |
| Breadboard | Circuit Setup |
| Jumper Wires | Connections |
| Power Supply | Device Power |

---

## 💻 Software Requirements

- Arduino IDE
- Embedded C/C++
- ESP32/ESP8266 Board Package
- IoT Cloud Platform

Supported Platforms:

- Blynk
- ThingSpeak
- Firebase
- MQTT Server

---

## ⚙️ Working Principle

1. Temperature and humidity sensors collect environmental data.
2. Rain sensor detects rainfall conditions.
3. ESP32 receives all sensor values.
4. Microcontroller processes the collected information.
5. Data is transmitted to an online server using WiFi.
6. Users can view live weather information remotely.
7. Alerts are generated if values exceed the selected threshold.

---

## 🔄 System Flow
