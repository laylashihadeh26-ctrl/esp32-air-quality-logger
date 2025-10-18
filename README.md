![IAQ Monitor Cover Image](cover.png)
# Low-Cost Indoor Air Quality (IAQ) Monitoring System

## Overview
This project presents a low-cost indoor air quality (IAQ) monitoring system designed to evaluate ventilation effectiveness in indoor spaces.  
The system measures carbon dioxide (CO₂) and **particulate matter (PM₁.₀, PM₂.₅, PM₁₀) concentrations and logs the data to a microSD card for later analysis.  

Built on an ESP32 microcontroller, the device was deployed in the American University of Beirut weight room for a two-week monitoring period (July–August 2025).  
The recorded CO₂ decay curves were used to estimate air change rates (ACR) and assess compliance with ASHRAE Standard 62.1 ventilation requirements.

---

## Repository Contents
- **`IAQ_monitor.ino`** – Main Arduino/ESP32 firmware controlling the sensors and data logging.  
- **`gym_iaq_data.csv`** – Example dataset collected during deployment.  
- **`README.md`** – Project documentation (this file).

---

## Hardware Requirements
- **ESP32 microcontroller**  
- **CO₂ sensor** (MH-Z19)  
- **Particulate matter (PM) sensor** (Plantower PMS5003)  
- **microSD card module**  
- **Power supply** and **protective enclosure**

---
## Bill of Materials (Estimated Cost)
The following table lists all components used in the IAQ monitoring system, along with their approximate quantities and costs (USD) at the time of assembly.

| Component | Quantity | Cost (USD) |
|------------|-----------|------------|
| ESP32 development board (30 pin) | 1 | 7.0 |
| MH-Z14 CO₂ sensor | 1 | 32.0 |
| PMS5003 particulate matter sensor | 1 | 19.0 |
| MicroSD card module | 1 | 0.9 |
| MicroSD card (4 GB) | 1 | 4.0 |
| Perfboard | 2 | 0.4 |
| USB-A to USB-C cable | 2 | 4.0 |
| microUSB to USB-C adapter | 1 | 5.0 |
| Portable power bank (5 V output) | 1 | 6.0 |
| USB wall adapter | 1 | 6.0 |
| Jumper wires | 1 | 0.8 |
| **Total** | **12** | **≈ 89.5** |

---

## Software Requirements
- **Arduino IDE** (version 2.0 or later)
- Required Arduino libraries:
  - `SPI.h`
  - `SD.h` 

## Setup and Usage
1. Open `IAQ_monitor.ino` in the Arduino IDE.  
2. Install all required libraries listed above.  
3. Connect the sensors to the ESP32 according to the pin definitions in the code.  
4. Upload the firmware to the ESP32.  
5. Insert a formatted microSD card into the SD module.  
6. Power on the device to start data logging automatically.

Sensor readings (CO₂ and PM values with timestamps) are saved to the microSD card in CSV format.

---

## Data Analysis
The provided `data.csv` file demonstrates the data format and structure.  
CO₂ decay data can be analyzed using exponential regression to estimate **Air Change Rate (ACR)**.  
The calculated ACR values can then be compared to **ASHRAE Standard 62.1** ventilation requirements to evaluate indoor air quality performance.

---
## Citation
If you use or reference this project, please cite it as:

> Shihadeh, L. (2025). *Low-Cost Indoor Air Quality Monitoring System for Evaluating Ventilation in Indoor Environments.* American University of Beirut. Available at: (https://github.com/laylashihadeh26-ctrl/esp32-air-quality-logger)

## License
This project is released under the **MIT License**, allowing free use, modification, and distribution with attribution.

---

## Contact
For questions or collaboration, please contact:  
**Layla Shihadeh** – laylashihadeh26@gmail.com  

