# IoT-Based Smart Medical Supply Storage & Cold-Chain Monitoring System

> A low-cost IoT-based system for monitoring temperature, humidity, door status, and storage conditions of a medical supply container with a web-based monitoring dashboard.

---

## 📌 Project Overview

Medical supplies that require controlled storage conditions need regular monitoring of environmental factors such as temperature and humidity.

Traditional manual monitoring can be time-consuming and may fail to detect abnormal conditions immediately.

This project proposes an **IoT-Based Smart Medical Supply Storage and Cold-Chain Monitoring System** using an ESP32 microcontroller, sensors, Wi-Fi, Node.js, Express.js, MongoDB, and Next.js.

The system continuously collects environmental data from a storage container and sends the data to a backend server. The collected information is stored in MongoDB and displayed through a web-based dashboard.

If an abnormal condition is detected, the system can generate a local and dashboard-based alert.

> **Important:** This is an undergraduate educational prototype. It is not a certified medical or pharmaceutical cold-chain monitoring system.

---

# 🎯 Main Objective

The main objective of this project is to develop a **low-cost IoT-based monitoring system that continuously observes the environmental conditions of a medical supply storage container and provides timely alerts when abnormal conditions are detected.**

---

# ❗ Problem Statement

Manual monitoring of medical supply storage conditions can result in delayed detection of abnormal temperature or humidity.

For example:

```text
Manual Monitoring
       ↓
Periodic Checking
       ↓
Abnormal Condition
       ↓
May remain unnoticed
       ↓
Potential Supply Damage
