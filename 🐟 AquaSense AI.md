# 🐟 AquaSense AI

### AIoT-Based Intelligent Fish Farm Monitoring, Prediction & Automated Management System

AquaSense AI is an **AI + IoT-based smart fish farming system** designed to help fish farmers monitor water quality, detect abnormal conditions, optimize feeding, predict fish health risks, and automate important farm operations.

The system combines **ESP32, IoT sensors, MQTT, Node.js, MongoDB, React/Next.js, and Machine Learning** to create an intelligent and real-time fish farm management platform.

---

## 📌 Project Overview

Traditional fish farming often depends heavily on manual observation and experience. Farmers may not continuously monitor important water parameters such as:

* Temperature
* pH
* Dissolved Oxygen (DO)
* Turbidity
* Water level

Sudden changes in these parameters can negatively affect fish health and farm productivity.

AquaSense AI addresses this problem by continuously collecting environmental data through IoT sensors and using AI/ML models to analyze the data and provide actionable insights.

### Core Pipeline

```text
Fish Pond
    ↓
IoT Sensors
    ↓
ESP32
    ↓
Wi-Fi / MQTT
    ↓
Backend Server
    ↓
MongoDB
    ↓
AI/ML Service
    ↓
Prediction & Decision
    ↓
Web Dashboard
    ↓
Farmer Alert / Automation
```

---

# 🎯 Objectives

The main objectives of AquaSense AI are:

1. Monitor fish pond conditions in real time.
2. Collect water-quality data automatically.
3. Detect abnormal environmental conditions.
4. Predict fish health risks using Machine Learning.
5. Provide intelligent feeding recommendations.
6. Predict future water-quality conditions.
7. Automate aerator control based on water conditions.
8. Provide real-time alerts to farmers.
9. Maintain historical farm data.
10. Help farmers make data-driven decisions.

---

# 🚀 Key Features

## 🌡️ Real-Time Water Monitoring

The system continuously monitors:

* Water Temperature
* pH
* Dissolved Oxygen
* Turbidity
* Water Level
* Air Temperature
* Humidity

---

## 🤖 AI Fish Health Risk Prediction

The AI model analyzes environmental conditions and predicts potential fish health risks.

Example:

```text
Temperature: 31°C
pH: 8.4
DO: 3.2 mg/L
Turbidity: HIGH

AI Prediction:
HIGH RISK ⚠️

Recommendation:
Increase aeration and inspect pond conditions.
```

The prediction is intended as a decision-support feature and not as a substitute for professional aquaculture or veterinary advice.

---

## 🍚 AI-Based Smart Feeding

Instead of feeding fish only according to a fixed schedule, the system can consider:

* Fish age
* Fish population
* Average fish weight
* Water temperature
* Previous feeding amount
* Historical growth
* Water conditions

The AI model can generate an estimated feeding recommendation.

Example:

```text
Recommended Feed:
1.8 KG

Prediction Confidence:
87%

Reason:
Fish growth + temperature + historical feeding data
```

---

## 💨 Automatic Aerator Control

The system can automatically control an aerator according to configured dissolved-oxygen conditions.

```text
DO decreases
      ↓
ESP32 detects condition
      ↓
System evaluates threshold
      ↓
Aerator ON
      ↓
DO improves
      ↓
Aerator OFF
```

For a physical prototype, appropriate electrical isolation and safe low-voltage switching hardware must be used.

---

## 🚨 Anomaly Detection

The system can detect unusual sensor behavior.

Example:

```text
Normal DO:

5.2
5.0
4.9
5.1
5.0

Sudden Reading:

2.1 ⚠️
```

The system can generate:

```text
ANOMALY DETECTED

Pond: Farm-01
Parameter: Dissolved Oxygen
Severity: HIGH
```

---

## 📈 Water Quality Prediction

The AI component can estimate future water conditions based on historical sensor readings.

Example:

```text
Current Water Quality:
GOOD ✅

Predicted Next 6 Hours:
GOOD

Risk Probability:
12%
```

---

## 🐟 Fish Growth Prediction

Farmers can provide information such as:

```text
Species: Tilapia
Age: 90 Days
Average Weight: 120g
Population: 1500
```

The system can estimate future growth based on available historical data.

---

## 🔔 Smart Alert System

The system can generate alerts for:

* Low dissolved oxygen
* Abnormal pH
* High temperature
* High turbidity
* Abnormal water level
* Sensor failure
* Fish health risk
* Predicted water-quality deterioration

Possible notification channels:

* Web notifications
* Email
* SMS
* Mobile notifications

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │     Fish Pond       │
                    └──────────┬──────────┘
                               │
                     ┌─────────▼─────────┐
                     │    IoT Sensors    │
                     │                   │
                     │ Temperature       │
                     │ pH                │
                     │ Dissolved Oxygen  │
                     │ Turbidity         │
                     │ Water Level       │
                     └─────────┬─────────┘
                               │
                               ▼
                         ┌───────────┐
                         │   ESP32   │
                         └─────┬─────┘
                               │
                             Wi-Fi
                               │
                              MQTT
                               │
                    ┌──────────▼──────────┐
                    │    Node.js API      │
                    │      Express        │
                    └──────────┬──────────┘
                               │
                         ┌─────▼─────┐
                         │  MongoDB  │
                         └─────┬─────┘
                               │
                    ┌──────────▼──────────┐
                    │     AI Service      │
                    │                     │
                    │ Health Prediction   │
                    │ Feed Prediction     │
                    │ Anomaly Detection   │
                    │ Water Prediction    │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │  Web Dashboard      │
                    │ React / Next.js     │
                    └─────────────────────┘
```

---

# 🛠️ Technology Stack

## Hardware

* ESP32
* pH Sensor
* Temperature Sensor
* Dissolved Oxygen Sensor
* Turbidity Sensor
* Water Level Sensor
* Humidity Sensor
* Relay Module
* Aerator
* Power Supply

---

## Frontend

* React.js / Next.js
* JavaScript / TypeScript
* Tailwind CSS
* Recharts
* Axios

---

## Backend

* Node.js
* Express.js
* REST API
* MQTT
* JWT Authentication

---

## Database

* MongoDB
* Mongoose

---

## AI / Machine Learning

* Python
* FastAPI
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* PyTorch (optional)

---

## Communication

```text
ESP32
  ↓
Wi-Fi
  ↓
MQTT
  ↓
Backend
```

---

# 📊 Data Collection

The system stores sensor information with timestamps.

Example:

```json
{
  "pondId": "POND-001",
  "temperature": 29.4,
  "ph": 7.6,
  "dissolvedOxygen": 5.1,
  "turbidity": 3.2,
  "waterLevel": 82,
  "timestamp": "2026-08-17T10:30:00Z"
}
```

---

# 🧠 AI Pipeline

```text
Sensor Data
     ↓
Data Collection
     ↓
Data Cleaning
     ↓
Feature Engineering
     ↓
Dataset
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Prediction API
     ↓
Dashboard
```

### Potential ML Models

| Problem                  | Possible Model             |
| ------------------------ | -------------------------- |
| Fish Health Risk         | Random Forest / XGBoost    |
| Feed Recommendation      | Random Forest / Regression |
| Anomaly Detection        | Isolation Forest           |
| Water Quality Prediction | Random Forest / XGBoost    |
| Time-Series Prediction   | LSTM / GRU                 |
| Fish Growth Prediction   | Regression                 |

The final model should be selected based on the quality and quantity of collected data.

---

# 🗃️ Proposed Database Structure

```text
users
│
├── farmers
│
└── admins

farms
│
├── farm information
├── owner
└── location

ponds
│
├── pond information
├── fish species
└── fish population

sensor_readings
│
├── temperature
├── pH
├── dissolved oxygen
├── turbidity
├── water level
└── timestamp

feeding_records
│
├── amount
├── time
└── fish population

alerts
│
├── type
├── severity
├── message
└── timestamp

predictions
│
├── health risk
├── water quality
├── feeding recommendation
└── confidence
```

---

# 📁 Project Structure

A possible monorepo structure:

```text
AquaSense-AI/
│
├── client/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── services/
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── services/
│   └── config/
│
├── ai-service/
│   ├── models/
│   ├── dataset/
│   ├── training/
│   ├── preprocessing/
│   ├── prediction/
│   └── main.py
│
├── iot/
│   ├── esp32/
│   ├── sensors/
│   └── mqtt/
│
├── docs/
│   ├── architecture/
│   ├── research/
│   └── diagrams/
│
├── README.md
└── LICENSE
```

---

# 👥 Team Responsibilities

For a 4-member team:

### Member 1 — IoT & Hardware

* ESP32 programming
* Sensor integration
* MQTT communication
* Aerator automation
* Hardware testing

### Member 2 — Backend

* Node.js
* Express.js
* MongoDB
* REST API
* Authentication
* MQTT integration

### Member 3 — AI/ML

* Dataset preparation
* Data preprocessing
* Model development
* Model evaluation
* Prediction API

### Member 4 — Frontend

* React/Next.js
* Dashboard
* Charts
* Alerts
* Farm management UI
* Responsive design

All members should contribute to documentation, testing and research.

---

# 🔐 Security

The system should implement:

* JWT authentication
* Password hashing
* Role-based access control
* API validation
* MQTT authentication
* Environment variables
* Rate limiting
* Secure database access

Never commit:

```text
.env
API keys
Database passwords
MQTT credentials
Private certificates
```

---

# 📈 Future Improvements

Possible future development:

* 📱 Android/iOS mobile application
* 🛰️ Satellite/weather data integration
* 🌦️ Weather-aware feeding
* 🐟 Computer vision for fish counting
* 📷 Camera-based fish behavior analysis
* 🧠 Deep-learning-based disease detection
* 🗺️ Multi-farm management
* ☁️ Cloud IoT deployment
* 📊 Advanced predictive analytics
* 🔊 Voice alerts
* 🌐 Bengali farmer interface

---

# 🎓 Academic / Research Potential

AquaSense AI can be developed as a:

* University project
* IoT project
* AI/ML project
* Final-year project
* Research project
* Thesis prototype

Potential research direction:

> **AIoT-Based Intelligent Monitoring and Predictive Management of Aquaculture Water Quality**

Possible research questions:

1. Can IoT sensor data reliably monitor fish-pond conditions?
2. Can ML models predict fish health risk from environmental parameters?
3. Can AI improve feeding decisions?
4. Can anomaly detection identify potentially dangerous water conditions earlier?
5. Can automated aeration reduce unnecessary energy consumption?

---

# ⚠️ Important Limitation

AquaSense AI is an academic/research prototype.

AI predictions should be treated as **decision-support recommendations**, not guaranteed biological outcomes.

Sensor calibration, environmental variation, fish species, stocking density, weather and farm-management practices can significantly affect results.

For real-world deployment, the system should undergo proper sensor calibration, field testing and validation with aquaculture experts.

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone https://github.com/your-username/AquaSense-AI.git

cd AquaSense-AI
```

## 2. Install Frontend

```bash
cd client
npm install
npm run dev
```

## 3. Install Backend

```bash
cd server
npm install
npm run dev
```

## 4. Setup AI Service

```bash
cd ai-service

python -m venv venv
```

Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run:

```bash
uvicorn main:app --reload
```

---

# ⚙️ Environment Variables

Create `.env` files for the required services.

Example:

```env
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret
MQTT_BROKER=your_mqtt_broker
MQTT_USERNAME=your_username
MQTT_PASSWORD=your_password
AI_SERVICE_URL=http://localhost:8000
```

Never upload real credentials to GitHub.

---

# 🧪 Development Roadmap

## Phase 1 — Research

* [ ] Define problem statement
* [ ] Literature review
* [ ] Identify research gap
* [ ] Select fish species
* [ ] Select sensors
* [ ] Design architecture

## Phase 2 — IoT

* [ ] ESP32 setup
* [ ] Temperature sensor
* [ ] pH sensor
* [ ] DO sensor
* [ ] Turbidity sensor
* [ ] Water-level sensor
* [ ] MQTT communication

## Phase 3 — Backend

* [ ] Node.js setup
* [ ] MongoDB setup
* [ ] Authentication
* [ ] Sensor API
* [ ] Farm API
* [ ] Alert API

## Phase 4 — Frontend

* [ ] Dashboard
* [ ] Live sensor data
* [ ] Charts
* [ ] Farm management
* [ ] Alerts
* [ ] AI predictions

## Phase 5 — AI

* [ ] Collect dataset
* [ ] Clean dataset
* [ ] Feature engineering
* [ ] Train models
* [ ] Evaluate models
* [ ] Deploy prediction API

## Phase 6 — Automation

* [ ] Aerator control
* [ ] Smart feeding prototype
* [ ] Automated alerts
* [ ] Safety testing

## Phase 7 — Testing

* [ ] Sensor calibration
* [ ] Hardware testing
* [ ] API testing
* [ ] AI evaluation
* [ ] End-to-end testing
* [ ] Field testing

## Phase 8 — Documentation

* [ ] Project report
* [ ] Research paper
* [ ] System diagrams
* [ ] Dataset documentation
* [ ] Final presentation
* [ ] Demo video

---

# 📜 License

This project is developed for educational and research purposes.

Choose an appropriate open-source license before public release.

---

# 👨‍💻 Team

**Project:** AquaSense AI

**Category:** AI + IoT + Smart Agriculture + Aquaculture

**Development:** 4-Member Team

**Status:** 🚧 In Development

---

# ⭐ Vision

> **“Making fish farming smarter through IoT, Artificial Intelligence and data-driven decision making.”**

---

## 📌 Keywords

```text
AI
Artificial Intelligence
IoT
AIoT
ESP32
Smart Fish Farm
Smart Aquaculture
Fish Farming
Aquaculture
Machine Learning
Water Quality Monitoring
Fish Health Prediction
Smart Feeding
MQTT
MongoDB
Node.js
React
Next.js
Python
FastAPI
Smart Agriculture
Precision Aquaculture
```

