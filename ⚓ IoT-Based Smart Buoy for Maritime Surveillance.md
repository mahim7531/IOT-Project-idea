# ⚓ IoT-Based Smart Buoy for Maritime Surveillance

An IoT-based smart buoy system designed for **maritime environmental monitoring, buoy position tracking, abnormal movement detection, and real-time remote monitoring**.

The system uses sensors, GPS, wireless communication, and a cloud-based dashboard to collect and visualize real-time information from a floating buoy. The buoy can also be powered using a **solar energy system**, making it suitable for long-duration deployment.

---

## 📌 Project Overview

The **Smart Buoy for Maritime Surveillance** is an IoT project that combines embedded systems, GPS, wireless communication, cloud computing, and web technologies.

A floating buoy is equipped with multiple sensors that continuously collect information such as:

* 📍 GPS Location
* 🌊 Motion/Wave Activity
* 🌡️ Water Temperature
* 🔋 Battery Level
* ☀️ Solar Power Status

The collected data is transmitted to a remote server and displayed through a web-based monitoring dashboard.

If the system detects unusual movement or the buoy moves outside its predefined geographical area, an alert can be generated for the monitoring/control center.

---

## 🎯 Objectives

The main objectives of this project are:

* Monitor the real-time location of a smart buoy.
* Detect abnormal buoy movement.
* Monitor water temperature.
* Monitor battery and solar power status.
* Transmit sensor data wirelessly.
* Store sensor data in a database.
* Display real-time information through a web dashboard.
* Implement GPS-based geofencing.
* Generate alerts for abnormal conditions.
* Develop a low-power solar-powered IoT system.

---

## 🚀 Key Features

### 1. 📍 GPS Tracking

The system continuously obtains the buoy's geographical location using a GPS module.

The dashboard can display:

* Latitude
* Longitude
* Location history
* Current position
* Movement distance

---

### 2. 🌊 Wave & Motion Monitoring

An accelerometer and gyroscope can be used to monitor the movement of the buoy.

The system can detect:

* Normal movement
* Excessive movement
* Sudden movement
* Possible displacement

---

### 3. 🌡️ Water Temperature Monitoring

A waterproof temperature sensor measures the surrounding water temperature.

The data can be displayed as:

```text
Current Temperature: 28.6°C
```

Historical temperature data can also be stored for analysis.

---

### 4. 🚨 Geofencing & Movement Alert

A predefined geographical area can be configured for the buoy.

If the buoy moves outside the permitted area:

```text
⚠️ ALERT

Buoy movement detected!

Current Location:
Latitude: XX.XXXX
Longitude: XX.XXXX
```

The system can send the alert to the monitoring dashboard.

---

### 5. 🔋 Battery Monitoring

The system monitors the battery voltage/percentage.

Example:

```text
Battery: 82%
Status: Normal
```

If the battery becomes critically low:

```text
⚠️ LOW BATTERY ALERT
```

---

### 6. ☀️ Solar Power

The buoy can use a solar panel to charge its battery.

Basic power architecture:

```text
Solar Panel
     ↓
Charge Controller
     ↓
Rechargeable Battery
     ↓
Voltage Regulator
     ↓
ESP32 + Sensors + Communication Module
```

---

### 7. 📡 Wireless Communication

Depending on deployment requirements, the system can use:

* LoRa
* GSM
* 4G
* NB-IoT
* Wi-Fi (for prototype/testing)

For an IoT prototype, **MQTT** can be used for efficient sensor-data communication.

---

# 🧩 Hardware Components

| Component                 | Purpose                |
| ------------------------- | ---------------------- |
| ESP32                     | Main microcontroller   |
| GPS Module                | Location tracking      |
| MPU6050                   | Motion detection       |
| DS18B20 Waterproof Sensor | Water temperature      |
| LoRa/GSM/4G Module        | Wireless communication |
| Solar Panel               | Renewable power source |
| Rechargeable Battery      | Energy storage         |
| Solar Charge Controller   | Battery charging       |
| Voltage Sensor            | Battery monitoring     |
| Buzzer/LED                | Local alert            |
| Waterproof Enclosure      | Protect electronics    |

---

# 💻 Software & Technologies

## Embedded System

* C/C++
* Arduino IDE
* ESP32

## Communication

* MQTT
* LoRa / GSM / 4G
* REST API

## Backend

* FastAPI / Node.js
* Python / JavaScript
* MQTT Broker

## Database

* MongoDB

## Frontend

* React.js
* Next.js
* Tailwind CSS

## Map

* OpenStreetMap
* Leaflet.js

---

# 🏗️ System Architecture

```text
                  ☀️ Solar Panel
                       │
                       ▼
                🔋 Battery System
                       │
                       ▼
                    ESP32
              ┌────────┼─────────┐
              │        │         │
              ▼        ▼         ▼
             GPS     MPU6050   DS18B20
              │        │         │
              └────────┼─────────┘
                       │
                       ▼
              Sensor Data Processing
                       │
                       ▼
             LoRa / GSM / 4G / MQTT
                       │
                       ▼
                  Cloud Server
                       │
                       ▼
              FastAPI / Node.js
                       │
                       ▼
                   MongoDB
                       │
                       ▼
               Web Dashboard
                       │
                       ▼
                ⚓ Control Room
```

---

# 🔄 Data Flow

```text
Sensors
   ↓
ESP32
   ↓
Data Processing
   ↓
Wireless Communication
   ↓
MQTT / API
   ↓
Backend Server
   ↓
MongoDB
   ↓
Web Dashboard
   ↓
Alert System
```

---

# 🖥️ Dashboard

The monitoring dashboard can contain the following sections:

### Live Map

```text
┌─────────────────────────────────────┐
│          LIVE BUOY LOCATION         │
│                                     │
│              📍                     │
│                                     │
│       Latitude: XX.XXXX             │
│       Longitude: XX.XXXX            │
└─────────────────────────────────────┘
```

### Sensor Information

```text
🌡️ Water Temperature: 28.6°C

🌊 Motion Status: Normal

📍 GPS Status: Connected

🔋 Battery: 82%

☀️ Solar Status: Charging
```

### Alert Panel

```text
⚠️ Movement Alert
⚠️ Low Battery
⚠️ GPS Disconnected
⚠️ Communication Failure
```

---

# 🚨 Alert System

The system can generate alerts for:

* Abnormal movement
* Geofence violation
* Low battery
* GPS failure
* Sensor failure
* Communication failure
* Excessive motion

Possible notification methods:

* Dashboard notification
* Email
* SMS
* Telegram/other messaging integration

---

# 📊 Example MQTT Data

Example sensor payload:

```json
{
  "buoy_id": "BUOY-001",
  "latitude": 22.5001,
  "longitude": 91.7002,
  "water_temperature": 28.6,
  "motion_status": "NORMAL",
  "battery": 82,
  "solar_status": "CHARGING"
}
```

---

# 🗄️ Database Structure

Example MongoDB document:

```json
{
  "buoy_id": "BUOY-001",
  "location": {
    "latitude": 22.5001,
    "longitude": 91.7002
  },
  "water_temperature": 28.6,
  "motion": {
    "x": 0.12,
    "y": 0.18,
    "z": 0.95
  },
  "battery": 82,
  "solar_status": "CHARGING",
  "timestamp": "2026-08-25T12:00:00Z"
}
```

---

# 📁 Project Structure

```text
smart-buoy/
│
├── firmware/
│   ├── src/
│   │   ├── main.cpp
│   │   ├── gps.cpp
│   │   ├── motion.cpp
│   │   ├── temperature.cpp
│   │   └── communication.cpp
│   └── README.md
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   └── mqtt/
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── maps/
│   └── package.json
│
├── hardware/
│   ├── circuit/
│   ├── schematic/
│   └── images/
│
├── docs/
│   ├── architecture.png
│   ├── circuit-diagram.png
│   └── project-report.pdf
│
└── README.md
```

---

# ⚙️ Installation & Setup

## 1. Clone Repository

```bash
git clone https://github.com/your-username/smart-buoy.git

cd smart-buoy
```

---

## 2. Firmware Setup

Install:

* Arduino IDE
* ESP32 Board Package
* Required sensor libraries

Configure:

```text
Wi-Fi / GSM / LoRa
MQTT Broker
GPS
Sensor Pins
```

Upload the firmware to the ESP32.

---

## 3. Backend Setup

```bash
cd backend

python -m venv venv
```

Activate environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run server:

```bash
uvicorn app.main:app --reload
```

---

## 4. Frontend Setup

```bash
cd frontend

npm install

npm run dev
```

Open the dashboard in your browser.

---

# 🔐 Security Considerations

Because the system may be deployed in a sensitive maritime environment, communication and authentication should be designed securely.

Recommended measures:

* MQTT authentication
* TLS/SSL encryption
* API authentication
* JWT-based authorization
* Secure device credentials
* Encrypted communication
* Input validation
* Device ID verification

The prototype should use **simulated/test data and controlled environments** rather than being connected to real operational naval systems.

---

# 📈 Future Improvements

Future versions can include:

* 🤖 AI-based abnormal movement detection
* 📡 Long-range LoRa mesh communication
* 🛰️ Satellite communication
* 🌊 Wave-height estimation
* 🌦️ Weather monitoring
* 🔋 AI-based energy optimization
* 📊 Predictive maintenance
* 🗺️ Multi-buoy monitoring
* 📱 Android monitoring application
* 🔔 Advanced real-time notification system

---

# 🎓 Academic Value

This project combines several important CSE/IoT concepts:

* Internet of Things
* Embedded Systems
* Wireless Communication
* Sensor Networks
* GPS Technology
* MQTT
* Cloud Computing
* Database Management
* REST API
* Web Development
* Real-Time Data Visualization
* Geofencing
* Cybersecurity

Therefore, the project is suitable for a **CSE final-year project, IoT project, or undergraduate thesis prototype**.

---

# 👨‍💻 Contributors

**Project Team:**
CSE Department

**Project:**
IoT-Based Smart Buoy for Maritime Surveillance

---

# 📜 License

This project is developed for **educational and research purposes**.

Use of the system in real-world maritime or defense environments requires appropriate authorization, safety testing, and compliance with applicable regulations.

