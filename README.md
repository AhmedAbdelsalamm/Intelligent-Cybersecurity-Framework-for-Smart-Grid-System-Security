# Intelligent Cybersecurity System for Smart Grid Protection

##  Overview
This project presents a smart cybersecurity system designed to protect Smart Grid infrastructures from cyber attacks in real time.  
The system integrates **AI-based network traffic analysis** with **hardware control mechanisms** to detect attacks and automatically respond in order to maintain system safety, stability, and reliability.

The proposed solution combines **Raspberry Pi, Arduino, ESP32, Ethernet communication, and AI models** to form an intelligent, layered security framework for Smart Grid environments.

---

##  System Architecture
The system is composed of three main layers:

### 1- Detection Layer (Raspberry Pi)
- A Raspberry Pi is connected to a network switch configured with **Port Mirroring**.
- All network traffic from the Smart Grid units is mirrored to the Raspberry Pi.
- An **AI-based anomaly detection model** analyzes the traffic in real time.
- When a cyber attack is detected, an alert is sent to the control server.

---

### 2- Control Layer (Arduino Server)
- The Arduino acts as a **central control server**.
- It receives attack notifications from the Raspberry Pi.
- Based on the system state, it sends control commands to the Smart Grid units.

**Normal Mode:**
- The Arduino sends commands to keep the Smart Grid operating normally.
- Cooling fans remain ON.

**Attack Mode:**
- The Arduino sends an alert signal to the Smart Grid units.
- Emergency protection actions are triggered automatically.

---

### 3- Execution Layer (Smart Grid Units)
The system includes **two Smart Grid units**, each consisting of:

- ESP32 microcontroller  
- W5500 Ethernet module  
- 2-Channel Relay Module (5V)  
- Dynamo with cooling fan (2-wire)  
- LED and Buzzer for alerts  
- I2C LCD 16x2 display  

Each ESP32 receives commands from the Arduino server and controls the connected hardware components accordingly.

---

##  Hardware Components
- Raspberry Pi (AI-based detection)
- Arduino (central control server)
- ESP32 (Smart Grid controller)
- W5500 Ethernet Module
- 2-Channel Relay Module (5V)
- Cooling Fan (Dynamo)
- LED & Buzzer
- I2C LCD 16x2 Display
- Network Switch (with Port Mirroring)

---

##  Network Communication Flow
1. Smart Grid units generate network traffic.
2. Traffic passes through a network switch.
3. Port mirroring sends a copy of all traffic to the Raspberry Pi.
4. The AI model analyzes traffic patterns.
5. Upon detecting an attack:
   - Raspberry Pi alerts the Arduino.
   - Arduino sends commands to ESP32 units.
6. ESP32 executes protection actions on the hardware level.

---

##  Attack Response Scenario
When a cyber attack is detected:
- The cooling fan is turned **OFF** using the relay module.
- The **LED and buzzer** are activated as alerts.
- The **LCD displays** a warning message:  
  **“Attack Detected”**
- The affected Smart Grid unit is isolated to prevent damage.

This automated response minimizes system damage and ensures safe operation.

---

##  Types of Detected Cyber Attacks
- Denial of Service (DoS / DDoS)
- Network Scanning
- Man-in-the-Middle (MITM)
- ARP Spoofing
- False Data Injection
- Abnormal Network Traffic Patterns

---

##  Technologies Used
- Python (AI / Machine Learning)
- Network Traffic Analysis
- Raspberry Pi OS
- Arduino IDE
- ESP32 Libraries
- Ethernet (W5500)
- TCP/IP Communication
- I2C & SPI Protocols

---

##  Project Features
- Real-time cyber attack detection
- AI-based anomaly detection
- Automated hardware-level response
- Centralized control architecture
- Smart Grid simulation environment
- Scalable and modular design

---

##  Project Information
- **Project Type:** Graduation Project  
- **Department:** Computer Engineering  
- **Academic Year:** 2025–2026  

---

##  Future Work
- Integration with WhatsApp and Telegram alert systems
- Improved user interface for monitoring
- Support for additional Smart Grid units
- Enhanced AI models for detecting more attack types
- System miniaturization and power optimization

---

##  Contact
For questions or collaboration, feel free to reach out.
Gmail: ahmedabdelsalam045@gmail.com
LinkedIn: https://www.linkedin.com/in/ahmed-abdelsalam045-345214232/

