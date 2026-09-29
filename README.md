# Intelligent RFID and Cloud-Based Inventory Tracking System for Healthcare Supply Chains

A real-time healthcare inventory tracking system that uses **RFID, ESP32, Wi-Fi connectivity, and cloud-based monitoring** to automate medicine inventory management.

The system is designed for hospital pharmacies, medical stores, and healthcare supply chains where maintaining accurate medicine stock information is important. RFID tags provide unique identification for medicine items, an RFID reader captures tag information, and an ESP32 microcontroller processes and transmits the data to a cloud platform. Inventory information can then be monitored remotely through a web-based/cloud dashboard.

---

##  Project Overview

Traditional medicine inventory management often depends on manual records or barcode-based scanning. These approaches can require significant manual effort and may make it difficult to maintain up-to-date stock information.

This project automates the inventory tracking process by:

- Identifying medicines using RFID tags
- Reading RFID tags automatically
- Processing tag information using an ESP32
- Transmitting inventory data through Wi-Fi
- Updating inventory information on a cloud platform
- Displaying system status locally using a 16×2 LCD
- Providing remote inventory monitoring through a cloud/web dashboard
- Supporting low-stock and inventory-status monitoring

The project report describes the system as an automated solution for healthcare inventory management. The overall objective is to reduce manual record maintenance and improve inventory visibility.

---

##  Objectives

- Automate medicine identification using RFID technology.
- Track medicine movement within the inventory system.
- Transmit RFID data from the ESP32 to a cloud platform.
- Maintain centralized inventory information.
- Reduce manual data-entry errors.
- Improve inventory auditing and stock monitoring.
- Enable remote access to inventory information.
- Help reduce medicine shortages and wastage.

---

##  System Architecture

The system follows this general data flow:

<img width="590" height="436" alt="{1FB8339D-A941-409A-82B6-A768D592EEF7}" src="https://github.com/user-attachments/assets/fbcd6695-54ad-467b-83a8-30f9797ed394" />

A 16×2 LCD is also connected to the ESP32 to provide local status information such as RFID detection and data transmission status.

The project report's block diagram illustrates the RFID reader feeding data to the microcontroller, followed by Wi-Fi/cloud communication and dashboard-based monitoring.

---

## How It Works

1. An RFID tag is attached to a medicine package.
2. The RFID reader detects the tag.
3. The unique RFID tag ID is captured.
4. The tag information is sent to the ESP32.
5. The ESP32 processes the received information.
6. The ESP32 transmits the data through Wi-Fi.
7. The cloud platform receives and stores the inventory information.
8. Inventory information is updated on the monitoring dashboard.
9. The LCD displays local system status.
10. The process repeats whenever another RFID tag is detected.

---

##  Key Features

### RFID-Based Identification
Each medicine item can be associated with a unique RFID identifier, allowing automated identification without manual data entry.

### Real-Time Inventory Monitoring
The system transmits scanned RFID information to the cloud platform so inventory activity can be monitored remotely.

### ESP32-Based Processing
The ESP32 acts as the central controller between the RFID reader, LCD, Wi-Fi connection, and cloud platform.

### Cloud Monitoring
Inventory information can be stored and monitored through a cloud-based dashboard.

### Inventory Status
The dashboard can display information such as:

- Medicine stock levels
- Recently scanned medicines
- Inventory updates
- Low-stock notifications/status
- Medicine-related inventory events

### Local LCD Feedback
A 16×2 LCD provides immediate feedback about RFID detection and system status.

---

## Technologies Used

### Hardware

| Component | Purpose |
|---|---|
| **ESP32** | Main microcontroller and Wi-Fi communication |
| **EM-18 RFID Reader** | Reads RFID tag IDs |
| **RFID Tags** | Unique identification of medicine items |
| **16×2 LCD** | Displays local system status |
| **Power Supply** | Provides power to the system |

### Software

| Technology | Purpose |
|---|---|
| **Embedded C / C++** | Microcontroller programming |
| **Arduino IDE** | Development, compilation, and ESP32 upload |
| **Wi-Fi** | Data communication |
| **Blynk / Cloud Platform** | Remote monitoring and dashboard |
| **PHP** | Backend/web processing described in the project report |
| **Database** | Storage and management of inventory information |
| **HTML/CSS/JavaScript** | Web-dashboard technologies described in the project report |

---



##  Dashboard

The cloud dashboard is used to monitor inventory activity remotely.

The demonstrated outputs include:

- RFID medicine stock information
- Recently scanned medicine entries
- Low-stock notifications/events
- Online device status
- Medicine quantity visualizations

Example medicine records shown in the project report include medicines such as **Amlodipine, Paracetamol, Atorvastatin, Metformin, and Levothyroxine**.

---

## Getting Started

### Prerequisites

You will need:

- ESP32 development board
- EM-18 RFID reader
- RFID tags
- 16×2 LCD
- Suitable power supply
- USB cable
- Computer with Arduino IDE
- Wi-Fi connection
- Configured cloud/Blynk account

### 1. Install Arduino IDE

Install Arduino IDE and configure the ESP32 development-board support.

### 2. Connect the Hardware

Connect the RFID reader and LCD to the ESP32 according to the circuit used in the project.

### 3. Configure Wi-Fi

Update the Wi-Fi credentials in the ESP32 program:

```cpp
char ssid[] = "YOUR_WIFI_NAME";
char pass[] = "YOUR_WIFI_PASSWORD";
```

### 4. Configure Cloud Credentials

Add your own cloud/Blynk credentials rather than committing private credentials to GitHub.

```cpp
#define BLYNK_TEMPLATE_ID "YOUR_TEMPLATE_ID"
#define BLYNK_TEMPLATE_NAME "YOUR_TEMPLATE_NAME"
#define BLYNK_AUTH_TOKEN "YOUR_AUTH_TOKEN"
```

### 5. Select ESP32 Board

In Arduino IDE:

```text
Tools → Board → ESP32 → Select your ESP32 board
```

### 6. Upload the Program

Connect the ESP32 through USB, select the appropriate COM port, compile the program, and upload it.

### 7. Test RFID Scanning

Place an RFID tag within the reader's detection range and verify:

- Tag detection
- ESP32 processing
- LCD status
- Cloud communication
- Dashboard update

---

##  Security Note

**Never upload real Wi-Fi passwords, cloud authentication tokens, API keys, or other credentials to GitHub.**

Use placeholders such as:

```cpp
YOUR_WIFI_NAME
YOUR_WIFI_PASSWORD
YOUR_AUTH_TOKEN
```



##  Results

The implemented system demonstrates automated medicine inventory monitoring.

The project report documents successful RFID detection, transmission of RFID information through the ESP32, cloud-based monitoring, and dashboard visualization. The demonstrated dashboard outputs include medicine stock information, inventory events, and low-stock notifications.

The system is intended to reduce manual inventory work and provide more timely visibility into medicine stock.

---

##  Future Enhancements

Possible extensions described in the project include:

- Mobile application integration
- Integration with hospital management systems
- Automated billing and checkout
- Medicine expiry-date alerts
- Multi-location inventory management
- Role-based access control
- Encrypted data transmission
- Barcode + RFID hybrid tracking
- Inventory analytics and reporting
- SMS/email notifications
- Scalable cloud infrastructure

A future research-oriented version could additionally investigate demand forecasting, anomaly detection, or predictive inventory optimization using historical inventory data.

---

##  Research Context

The project was developed around the application of RFID, IoT, and cloud technologies to healthcare inventory management.

The project report discusses related work covering:

- RFID in healthcare
- RFID-based inventory systems
- IoT-enabled inventory management
- Cloud-based healthcare systems
- Smart pharmacy management
- Healthcare supply-chain tracking

Selected references from the project report include work on RFID in healthcare, RFID medication management, IoT-driven inventory management, and cloud/IoT healthcare systems.

---


