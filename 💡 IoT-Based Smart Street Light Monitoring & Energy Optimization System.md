# 💡 IoT-Based Smart Street Light Monitoring & Energy Optimization System

## 📌 Project Overview

The **IoT-Based Smart Street Light Monitoring & Energy Optimization System** is a software-based IoT project designed to monitor and control street lights intelligently without requiring any physical IoT hardware.

The system uses **virtual sensors** to simulate real-world street light data such as light intensity, motion detection, brightness, power consumption, and light faults.

The main goal is to **reduce electricity consumption, automate street light operation, and detect faulty lights in real time**.

---

## 🎯 Objectives

* Automatically control street lights based on day/night conditions.
* Increase brightness when motion is detected.
* Reduce brightness when the road is empty.
* Monitor individual street lights in real time.
* Detect faulty street lights.
* Calculate electricity consumption.
* Display real-time data through a web dashboard.
* Reduce unnecessary energy consumption.
* Demonstrate IoT functionality without physical hardware.

---

## 🚀 Main Features

### 🌞 1. Day & Night Detection

The system uses a virtual light sensor to determine whether it is day or night.

```text
Light Intensity > 50%
        ↓
      DAY
        ↓
Street Lights OFF
```

```text
Light Intensity < 50%
        ↓
     NIGHT
        ↓
Street Lights ON
```

---

### 🚶 2. Motion Detection

When a vehicle or person is detected:

```text
Motion Detected
      ↓
Brightness = 100%
```

When there is no movement:

```text
No Motion
      ↓
Brightness = 30%
```

This helps reduce unnecessary electricity consumption.

---

### 💡 3. Automatic Brightness Control

The system dynamically adjusts brightness based on road activity.

| Condition         | Brightness |
| ----------------- | ---------: |
| Day               |         0% |
| Night + No Motion |        30% |
| Night + Motion    |       100% |

---

### ⚠️ 4. Fault Detection

The system continuously checks street light status.

Example:

```text
Expected Status: ON
Actual Status: OFF

⚠️ Street Light Fault Detected
```

The administrator can see faulty lights from the dashboard.

---

### 📊 5. Energy Monitoring

The system calculates estimated power consumption for each street light.

Example:

```text
Light #01
Brightness: 100%
Power: 45W

Light #02
Brightness: 30%
Power: 15W
```

The dashboard can display:

* Daily consumption
* Weekly consumption
* Monthly consumption
* Estimated electricity cost
* Energy saved

---

### 🖥️ 6. Real-Time Dashboard

The web dashboard displays:

* Total street lights
* Active lights
* Inactive lights
* Faulty lights
* Current brightness
* Motion status
* Light intensity
* Power consumption
* Energy savings
* Historical data

---

## 🏗️ System Architecture

```text
             ┌──────────────────────┐
             │ Virtual IoT Sensors  │
             │                      │
             │ • Light Sensor       │
             │ • Motion Sensor      │
             │ • Light Status       │
             └──────────┬───────────┘
                        │
                        ▼
                ┌───────────────┐
                │ MQTT / API    │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │ FastAPI       │
                │ Backend       │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │   MongoDB     │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │ React / Next  │
                │ Dashboard     │
                └───────────────┘
```

---

## 🛠️ Technology Stack

### Frontend

* React.js / Next.js
* Tailwind CSS
* Recharts
* Axios

### Backend

* Python
* FastAPI
* Pydantic
* Uvicorn

### Database

* MongoDB

### IoT Communication

* MQTT
* Python Virtual Sensor Simulator

### Development Tools

* VS Code
* Git
* GitHub
* Postman

---

## 📂 Project Structure

```text
smart-street-light/
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── routes/
│   │   ├── services/
│   │   └── database/
│   │
│   ├── requirements.txt
│   └── .env
│
├── frontend/
│   ├── app/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── public/
│   └── package.json
│
├── simulator/
│   ├── sensor_simulator.py
│   ├── motion_simulator.py
│   └── light_simulator.py
│
├── docs/
│   ├── architecture.png
│   └── project-report.pdf
│
├── .gitignore
└── README.md
```

---

## 🔄 System Workflow

```text
Start
  ↓
Generate Virtual Sensor Data
  ↓
Check Light Intensity
  ↓
Day or Night?
  ↓
Night
  ↓
Check Motion
  ↓
Motion Detected?
  ├── YES → Brightness 100%
  │
  └── NO  → Brightness 30%
  ↓
Calculate Power Consumption
  ↓
Check Light Fault
  ↓
Send Data to Backend
  ↓
Store Data in MongoDB
  ↓
Display Data on Dashboard
```

---

## 📡 Virtual Sensor Data

The simulator generates data such as:

```json
{
  "street_light_id": "SL-001",
  "light_intensity": 18,
  "motion_detected": true,
  "brightness": 100,
  "temperature": 32,
  "power_consumption": 45,
  "status": "ON"
}
```

The data is continuously sent to the backend to simulate a real IoT environment.

---

## 🗄️ Database Design

### Street Light Collection

```text
StreetLight
│
├── light_id
├── location
├── status
├── brightness
├── light_intensity
├── motion_detected
├── power_consumption
├── temperature
├── fault_status
└── updated_at
```

### Energy Collection

```text
Energy
│
├── light_id
├── date
├── energy_consumed
├── estimated_cost
└── energy_saved
```

---

## 🔌 API Examples

### Get All Street Lights

```http
GET /api/street-lights
```

### Get Specific Street Light

```http
GET /api/street-lights/{id}
```

### Update Street Light

```http
PUT /api/street-lights/{id}
```

### Get Energy Statistics

```http
GET /api/energy/statistics
```

### Get Faulty Lights

```http
GET /api/street-lights/faults
```

---

## 📈 Dashboard Statistics

Example dashboard:

```text
╔══════════════════════════════════════════╗
║       SMART STREET LIGHT DASHBOARD       ║
╠══════════════════════════════════════════╣
║                                          ║
║ Total Lights        50                   ║
║ Active Lights       43                   ║
║ Faulty Lights       2                   ║
║ Energy Saved       37%                   ║
║                                          ║
╠══════════════════════════════════════════╣
║ Light #01    🟢 ON      100%             ║
║ Light #02    🟢 ON       30%             ║
║ Light #03    🔴 FAULT     0%             ║
║ Light #04    🟢 ON      100%             ║
╚══════════════════════════════════════════╝
```

---

## 💰 Project Cost

This project is designed to work **without purchasing physical IoT hardware**.

| Component                | Cost |
| ------------------------ | ---: |
| ESP32                    |   ৳0 |
| LDR Sensor               |   ৳0 |
| Motion Sensor            |   ৳0 |
| LED                      |   ৳0 |
| Relay                    |   ৳0 |
| MQTT                     |   ৳0 |
| FastAPI                  |   ৳0 |
| React/Next.js            |   ৳0 |
| MongoDB                  |   ৳0 |
| Virtual Sensor Simulator |   ৳0 |

### Total Hardware Cost: **৳0**

Only a computer and internet connection are required for development.

---

## 🔮 Future Improvements

The project can be extended with:

* AI-based traffic prediction
* Machine learning for energy prediction
* GPS-based street light mapping
* SMS alerts
* Email notifications
* Mobile application
* Smart city integration
* Solar-powered street light support
* Real-time map visualization
* Automatic maintenance scheduling
* Real ESP32 hardware integration

---

## 🎓 Academic Value

This project demonstrates practical knowledge of:

* Internet of Things (IoT)
* MQTT communication
* REST API
* FastAPI
* React/Next.js
* MongoDB
* Real-time monitoring
* Automation
* Data visualization
* Energy optimization
* Fault detection

It can be used as a **university IoT project, CSE final-year project, or thesis prototype**.

---

## 👨‍💻 Author

**Md Tayam Hasan Mahim**

### Project

**IoT-Based Smart Street Light Monitoring & Energy Optimization System**

---

## ⭐ Conclusion

The Smart Street Light System provides an intelligent approach to street light management by combining **IoT concepts, automation, real-time monitoring, energy optimization, and fault detection**.

The system can be completely demonstrated through **software-based virtual sensors**, making it possible to develop and present the project without purchasing physical IoT devices.
