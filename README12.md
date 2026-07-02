
# 🐄 IoT-Based Dairy Cow Environmental Monitoring System Using ESP32 and LoRa

## Final Year Thesis Project

### Submitted By
**Group B**

- Md Tayam Hasan Mahim
- Emon Ahmed Rabby
- Lopa Roy
- Shemul Chandra Sarkar

### Institution
Delta Computer Science College

### Supervisor
Abdullah Al Mahmud

---

# Abstract

The IoT-Based Dairy Cow Environmental Monitoring System is a smart farming solution designed to continuously monitor the environmental conditions inside dairy farms. The system uses ESP32 microcontrollers, LoRa wireless communication, and multiple environmental sensors to collect real-time data such as temperature, humidity, and light intensity.

Collected data is transmitted wirelessly using LoRa technology from the monitoring node to a receiver node connected to a laptop. The receiver displays the data on a dashboard, stores it in CSV format for future analysis, and generates alerts whenever environmental conditions exceed predefined thresholds.

The proposed system provides a low-cost, energy-efficient, and long-range monitoring solution that helps farmers improve dairy cow welfare and reduce environmental stress.

---

# Project Objectives

- Develop a low-cost smart dairy farm monitoring system.
- Monitor environmental parameters in real time.
- Transmit sensor data using LoRa communication.
- Display live environmental data on a dashboard.
- Generate alerts during abnormal environmental conditions.
- Store collected data for future analysis.

---

# System Architecture

```

Temperature
Humidity
Light
Air Quality (Optional)

↓

ESP32 (Sender)

↓

LoRa SX1278

~~~~~~~~~~~~~~~~~~~~~~~~

LoRa SX1278

↓

ESP32 (Receiver)

↓

Laptop

↓

Dashboard

↓

CSV Data Logging

↓

Alert System

```

---

# Hardware Components

| Component | Quantity |
|------------|----------|
| ESP32 Dev Board | 2 |
| LoRa SX1278 Module | 2 |
| DHT22 Temperature & Humidity Sensor | 1 |
| BH1750 Light Sensor | 1 |
| MQ135 Air Quality Sensor (Optional) | 1 |
| Rain Sensor (Optional) | 1 |
| OLED Display (0.96") | 1 |
| Breadboard | 2 |
| Jumper Wires | 1 Set |
| USB Cable | 2 |

---

# Software Requirements

- Arduino IDE
- ESP32 Board Package
- LoRa Library
- DHT Library
- BH1750 Library
- Adafruit SSD1306 Library
- Adafruit GFX Library
- Python
- Streamlit (Dashboard)
- CSV Logger
- GitHub

---

# Features

- Real-time Temperature Monitoring
- Real-time Humidity Monitoring
- Light Intensity Monitoring
- Long-Range LoRa Communication
- OLED Display
- Dashboard Visualization
- CSV Data Logging
- Heat Stress Detection
- Low Humidity Alert
- Wireless Monitoring

---

# Project Workflow

## Phase 1
Literature Review

Topics

- Smart Farming
- Internet of Things
- Environmental Monitoring
- LoRa Communication

---

## Phase 2
Hardware Setup

Connect

- ESP32
- DHT22
- BH1750
- OLED
- LoRa Module

---

## Phase 3
Sensor Reading

Read

- Temperature
- Humidity
- Light
- Air Quality (Optional)

Display values on OLED.

---

## Phase 4
LoRa Communication

Sender ESP32

↓

LoRa

↓

Receiver ESP32

↓

Laptop

---

## Phase 5
Dashboard

Display

- Temperature
- Humidity
- Light
- Signal Strength
- Alert Status

---

## Phase 6
Alert System

Example

Temperature > 35°C

↓

Heat Stress Alert

Humidity < 40%

↓

Low Humidity Alert

---

## Phase 7
Data Logging

Example CSV

Time,Temperature,Humidity,Light

10:00,31,72,420

10:05,32,73,425

---

## Phase 8
Testing

Evaluate

- LoRa Range
- Packet Delivery Ratio
- Sensor Accuracy
- Battery Life
- System Reliability

---

# Expected Outputs

- Wireless LoRa Network
- Live Dashboard
- CSV Dataset
- Alert System
- Working Prototype
- Final Thesis Report

---

# Skills Gained

- ESP32 Programming
- LoRa Communication
- Smart Farming
- IoT System Design
- Embedded Systems
- Dashboard Development
- Data Logging
- Environmental Monitoring

---

# Future Improvements

- Soil Moisture Monitoring
- AI-Based Heat Stress Prediction
- Cloud Database Integration
- Mobile Application
- Solar Powered Monitoring Node
- GPS-Based Livestock Tracking

---

# Research Contribution

This project presents a low-cost IoT-based environmental monitoring system for dairy farms using ESP32 and LoRa technology. The proposed system enables long-range wireless communication, real-time environmental monitoring, automated alert generation, and data logging. It provides an affordable smart farming solution suitable for rural dairy farms where internet connectivity may be limited.

---

# License

This project is developed for academic and research purposes.

© 2026 Group B
Delta Computer Science College
