# 🌌 AstraLog Control

[![GitHub Pages](https://img.shields.io/badge/Deployed_on-GitHub_Pages-blue?logo=github)](https://simonereale.github.io/astralog-control/)

Welcome to **AstraLog Control**, the official documentation hub and web interface for the **AstraLog-HPC** project. 

This site serves as the central point of truth for our ESA-inspired spacecraft telemetry processing system, developed for the *Software Engineering for HPC* course (A.Y. 2025-2026).

**[Click here to access AstraLog Control](https://simonereale.github.io/astralog-control/)**

## 🚀 Key Features

### 1. Real-Time Fleet Monitoring
The central grid displays the operational status of the satellite fleet (e.g., **SAT_ALPHA**, **SAT_BETA**). Each satellite card allows you to:
*   **Verify Availability:** Instantly probe if the satellite's Digital Twin is actively broadcasting on the mission cluster.
*   **Throughput Analysis (Hz):** View a live chart of the packet arrival frequency (measured in Hertz). This is essential for verifying that your local Python collector is keeping up with the nominal mission bitrate.

### 2. Mission Assets & Configuration
Directly below the live telemetry monitors, you can download specific mission assets:
*   **Current Rules (JSON):** The set of monitoring rules (Simple, Rate, Stateful, Correlation) currently assigned to the satellite (the set of rules can change during the mission).
*   **Current Sensors (YAML):** The list of sensors currently active and their metadata (the list can change during the mission).
*   **Broker Endpoint:** The specific MQTT broker address for that satellite.

### 3. Mission Timeline & Progress
The **Mission Timeline** header tracks the project's lifecycle. A dynamic progress bar and a countdown show exactly how much time remains until the final mission closure (fixed at **Midnight on June 14, 2026 (GMT +1)**).

### 4. Mission Messages Log (Terminal)
The `Mission_Messages.log` terminal reports critical alerts from the instructors. Check this section regularly for updates regarding:
*   Changes to the Satellites fleet.
*   HiveMQ cluster maintenance windows.
*   Release of new templates or documentation.

---

## 🛠️ Technical Notes for Students

### MQTT Authentication
To connect your local collectors or C++ engines to the telemetry stream, use the credentials provided in the **🔑 Connection Auth** box:
*   **Standard Port (TLS):** 8883
*   **WebSockets Port (Dashboard):** 8884
*   **Protocol:** MQTT v5

---
*Developed by Simone Reale, Elisabetta Di Nitto*  
*Politecnico di Milano - Software Engineering for HPC*
