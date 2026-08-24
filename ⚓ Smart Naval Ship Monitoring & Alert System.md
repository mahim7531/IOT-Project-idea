
# ⚓ Smart Naval Ship Monitoring & Alert System

An IoT-based **Naval Ship Monitoring and Alert System** designed to monitor important environmental and operational parameters of a ship in real time.

The system uses sensors connected to an ESP32 to collect data such as temperature, humidity, water leakage, gas/smoke, vibration, battery status, and GPS location. The collected data is transmitted to a web-based dashboard for real-time monitoring and alerts.

> **Note:** This project is an educational IoT prototype for monitoring and safety purposes. It does not control weapons, navigation systems, or military equipment.

---

## 🚀 Features

* 🌡️ Real-time temperature monitoring
* 💧 Humidity monitoring
* 🌊 Water leakage detection
* 🔥 Smoke and gas detection
* 📳 Vibration monitoring
* 🔋 Battery status monitoring
* 📍 GPS-based location tracking
* 🚨 Real-time alert system
* 📊 Web-based monitoring dashboard
* 💾 Sensor data storage
* 📈 Historical sensor data visualization
* 🔔 Buzzer/LED warning system

---

## 🏗️ System Architecture

```text
                ┌─────────────────────┐
                │      Sensors        │
                │                     │
                │ DHT22               │
                │ Water Sensor        │
                │ MQ-2                │
                │ Vibration Sensor    │
                │ Battery Sensor      │
                │ GPS NEO-6M          │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │       ESP32         │
                │                     │
                │ Data Collection     │
                │ Processing          │
                │ Alert Detection     │
                └──────────┬──────────┘
                           │
                     Wi-Fi / Internet
                           │
                           ▼
                ┌─────────────────────┐
                │    Backend API      │
                │ Node.js + Express   │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │      MongoDB        │
                │   Sensor Database   │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Web Dashboard     │
                │ React.js            │
                │ Charts + GPS Map    │
                └─────────────────────┘
```

---

## 🔧 Hardware Requirements

| Component            | Purpose                   |
| -------------------- | ------------------------- |
| ESP32                | Main IoT controller       |
| DHT22                | Temperature & humidity    |
| Water Level Sensor   | Water leakage detection   |
| MQ-2                 | Smoke/gas detection       |
| Vibration Sensor     | Detect abnormal vibration |
| NEO-6M GPS           | Location tracking         |
| Buzzer               | Emergency warning         |
| LED                  | Status indication         |
| OLED/LCD             | Local data display        |
| Battery/Power Supply | System power              |

---

## 💻 Software Requirements

### Firmware

* Arduino IDE
* C/C++
* ESP32 Board Package

### Backend

* Node.js
* Express.js
* MongoDB
* REST API / MQTT

### Frontend

* React.js
* JavaScript
* CSS / Tailwind CSS
* Chart.js or Recharts
* Leaflet / OpenStreetMap

---

## 📂 Project Structure

```text
smart-naval-monitoring/
│
├── firmware/
│   ├── main.ino
│   ├── sensors.cpp
│   └── sensors.h
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   ├── package.json
│   └── README.md
│
├── docs/
│   ├── circuit-diagram.png
│   └── system-architecture.png
│
└── README.md
```

---

## 📊 Monitoring Parameters

### Temperature

The DHT22 sensor monitors the internal temperature.

Example:

```text
Temperature: 72°C
Status: ⚠️ HIGH
```

### Humidity

```text
Humidity: 65%
Status: 🟢 NORMAL
```

### Water Leakage

```text
Water Level: NORMAL
Status: 🟢 SAFE
```

If water is detected:

```text
🚨 WATER LEAKAGE DETECTED
```

### Smoke/Gas

The MQ-2 sensor detects abnormal smoke/gas levels.

```text
Gas Level: HIGH
🚨 WARNING!
```

### Vibration

The vibration sensor can detect abnormal vibration.

```text
Vibration: NORMAL
```

If abnormal vibration is detected:

```text
🚨 ABNORMAL VIBRATION DETECTED
```

### GPS

The GPS module provides the current prototype/device location.

```text
Latitude: 22.3569
Longitude: 91.7832
```

---

## 🚨 Alert System

The system can generate alerts when sensor values cross predefined thresholds.

Example:

```text
🚨 ALERT

Engine Room Temperature: 85°C

Status: CRITICAL
Action: Inspect the monitored area.
```

Alerts can be displayed on:

* Web dashboard
* OLED/LCD
* Buzzer
* LED
* Optional notification service

---

## 📱 Dashboard

The dashboard provides:

```text
┌──────────────────────────────────────────┐
│       ⚓ NAVAL MONITORING DASHBOARD      │
├──────────────────────────────────────────┤
│                                          │
│ 🌡 Temperature       72°C   🟢            │
│ 💧 Humidity          65%   🟢            │
│ 🌊 Water Level       SAFE  🟢            │
│ 🔥 Gas/Smoke         SAFE  🟢            │
│ 📳 Vibration         NORMAL 🟢           │
│ 🔋 Battery           87%   🟢            │
│                                          │
│ 📍 Device Location                       │
│                                          │
│             [ GPS MAP ]                  │
│                                          │
└──────────────────────────────────────────┘
```

---

## 🔄 Data Flow

```text
Sensors
   ↓
ESP32
   ↓
Wi-Fi
   ↓
Backend API / MQTT
   ↓
MongoDB
   ↓
React Dashboard
   ↓
Real-time Monitoring
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/smart-naval-monitoring.git

cd smart-naval-monitoring
```

### 2. Firmware Setup

Open:

```text
firmware/main.ino
```

in Arduino IDE.

Select:

```text
Board: ESP32
```

Configure your Wi-Fi credentials and upload the firmware.

---

### 3. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
```

Run the server:

```bash
npm run dev
```

---

### 4. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The dashboard will then be available through the local development URL shown by Vite.

---

## 🔐 Security

For a real deployment, the following security measures should be implemented:

* API authentication
* JWT-based authorization
* HTTPS/TLS
* Secure Wi-Fi configuration
* Environment variables for secrets
* Input validation
* Rate limiting
* Device authentication
* Database access control

---

## 📈 Future Improvements

Future versions may include:

* 🤖 Machine Learning-based predictive maintenance
* 📡 LoRaWAN for long-range telemetry
* ☁️ Cloud deployment
* 📱 Android/iOS monitoring application
* 🔔 Push notifications
* 📊 Advanced analytics
* 🧠 Anomaly detection
* 🔋 Solar-powered IoT node
* 🗺️ Multi-device fleet monitoring
* 📦 Multiple sensor nodes across different areas of the vessel

---

## 🎯 Project Objectives

The main objectives are:

1. Monitor ship-related environmental parameters.
2. Detect abnormal conditions early.
3. Provide real-time sensor information.
4. Track the IoT device's location.
5. Store historical sensor data.
6. Provide a centralized monitoring dashboard.
7. Demonstrate practical IoT and full-stack development skills.

---

## 🛠️ Technologies

```text
ESP32
C/C++
Arduino
DHT22
MQ-2
GPS NEO-6M
Node.js
Express.js
MongoDB
React.js
REST API
MQTT
Leaflet
Chart.js
```

---

## 👨‍💻 Author

**Md Tayam Hasan Mahim**

Computer Science & Engineering Student

---

## 📄 License

This project is intended for **educational and research purposes**.

The system is a civilian/educational monitoring prototype and is not designed for weapon control, targeting, or operational military use.
