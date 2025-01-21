# Overview

This project focuses on developing a real-time telemetry system for a [lucky dog racing league](https://www.racelucky.com/) race car. The system will monitor the vehicle's health, collect performance data, and transmit it wirelessly for analysis and visualization.

## Project Goals
- * **Real-time Vehicle Health Monitoring:**
	- Track critical parameters like temperatures and fuel levels.
- **Telemetry Data Acquisition and Storage:**
	- Collect comprehensive telemetry data for performance analysis.
	- Store data either locally or in a cloud-based solution.
- **Hardware Development:**
	- Design and manufacture a custom PCB using KiCAD.
- **Real-time Data Visualization:**
	- Dashboards and real-time graphing.
## System Components
* **Microcontroller:** STM32 (for data acquisition and processing)
* **Sensors:**
	* CAN bus (for vehicle data)
	* IMU (for acceleration and velocity)
	* GPS (for location and time synchronization)
* **Wireless Communication:** XBEE RF modules (for data transmission)
* **Data Serialization:** Postcard (using Serde for straightforward implementation)
* **Time-Series Database:**  Prometheus, and Grafana for data storage and analysis.