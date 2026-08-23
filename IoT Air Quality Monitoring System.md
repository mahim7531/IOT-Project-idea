
# 🌫️ IoT Air Quality Monitoring System

An IoT-based **Air Quality Monitoring System** that continuously measures air pollution levels and displays real-time environmental data. The system can detect harmful gases, temperature, humidity, and air quality and send the collected data to an online dashboard.

## 📌 Project Overview

Air pollution is a major environmental problem. This project uses IoT sensors to monitor the quality of air in real time.

The system collects data from different sensors and sends it to a microcontroller such as **ESP32/ESP8266**. The data can then be displayed on a web dashboard or mobile application.

## 🎯 Main Objectives

* Monitor air quality in real time
* Detect harmful gases and pollutants
* Measure temperature and humidity
* Display sensor data on an online dashboard
* Store historical air-quality data
* Send alerts when pollution exceeds a safe level

## 🛠️ Hardware Components

| Component    | Purpose                        |
| ------------ | ------------------------------ |
| ESP32        | Main IoT controller            |
| MQ-135       | Detect air pollutants/gases    |
| DHT11/DHT22  | Measure temperature & humidity |
| OLED Display | Display sensor readings        |
| Buzzer       | Pollution warning              |
| LED          | Status indication              |
| Wi-Fi        | Send data to cloud/server      |
| Jumper Wires | Circuit connection             |
| Breadboard   | Prototype development          |

## ⚙️ System Architecture

```text
        Air / Environment
              │
              ▼
        ┌─────────────┐
        │  MQ-135     │
        │ Air Sensor  │
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │ DHT11/DHT22 │
        │ Temp/Humidity│
        └──────┬──────┘
               │
               ▼
        ┌─────────────┐
        │    ESP32    │
        │ IoT Device  │
        └──────┬──────┘
               │ Wi-Fi
               ▼
        ┌─────────────┐
        │ Cloud/API   │
        │   Server    │
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │ Web Dashboard│
        └─────────────┘
               │
               ▼
       📊 Real-Time Data
```

## 🚀 Features

### 1. Real-Time Monitoring

The system continuously reads air-quality sensor data.

### 2. Temperature & Humidity Monitoring

DHT11/DHT22 measures environmental temperature and humidity.

### 3. Pollution Alert

When the air-quality value exceeds a predefined threshold, the system activates a buzzer and warning indicator.

### 4. Online Dashboard

Sensor data can be sent to a web server and displayed using graphs and charts.

### 5. Historical Data

The backend can store sensor readings in a database so users can view previous air-quality information.

### 6. Remote Monitoring

Users can monitor air quality remotely through a web application.

## 💻 Software & Technologies

### IoT

* ESP32
* Arduino IDE
* C/C++

### Backend

* Node.js
* Express.js
* REST API

### Database

* MongoDB

### Frontend

* React.js
* HTML
* CSS
* JavaScript

### Communication

* Wi-Fi
* HTTP/REST API

## 📊 Example Dashboard

The dashboard can display:

```text
Air Quality:       GOOD 🟢
Temperature:       28°C
Humidity:          65%
Pollution Level:   42
Device Status:     ONLINE 🟢
```

It can also contain:

* 📈 Air quality graph
* 🌡️ Temperature graph
* 💧 Humidity graph
* 📅 Historical data
* 🚨 Pollution alerts
* 📍 Device location

## 🔄 Working Process

1. Sensors collect environmental data.
2. ESP32 receives the sensor readings.
3. ESP32 processes the collected data.
4. ESP32 connects to the Internet using Wi-Fi.
5. Sensor data is sent to the backend API.
6. Backend stores the data in MongoDB.
7. React dashboard retrieves the data.
8. Users can monitor air quality in real time.
9. If pollution exceeds the threshold, an alert is generated.

## 📁 Suggested Project Structure

```text
air-quality-iot/
│
├── hardware/
│   └── esp32_air_quality.ino
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── circuit/
│   └── circuit-diagram.png
│
└── README.md
```

## 🔮 Future Improvements

* Add PM2.5 and PM10 sensors
* Add GPS location tracking
* Add mobile application
* Add SMS/email notifications
* Add AI-based pollution prediction
* Deploy dashboard to the cloud
* Add multiple IoT monitoring stations
* Create an air-quality map for different locations

## 👨‍💻 Applications

This project can be used for:

* 🏠 Smart homes
* 🏫 Schools and colleges
* 🏭 Industrial areas
* 🏥 Hospitals
* 🚦 Smart cities
* 🌳 Environmental monitoring
* 🏢 Offices

## 📜 License

This project is created for educational and research purposes.

## ⭐ Conclusion

The **IoT Air Quality Monitoring System** provides a low-cost solution for monitoring environmental conditions in real time. By combining **ESP32, sensors, IoT, REST API, MongoDB, and React**, the project demonstrates how IoT technology can be used to solve real-world environmental problems.
