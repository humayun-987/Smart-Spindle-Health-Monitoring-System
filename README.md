<!-- ![banner](media/User-Interface.png)

# Smart Spindle Health Monitoring System
**An intelligent, dual-platform spindle health monitoring system combining industrial-grade LabVIEW control with a cost-effective Raspberry Pi solution for real-time vibration-based fault detection.**

![License](https://img.shields.io/badge/license-MIT-green)  
![Platform](https://img.shields.io/badge/platform-LabVIEW%20%7C%20Raspberry%20Pi-blue)  
![Status](https://img.shields.io/badge/status-Completed-success)

---

## 📑 Table of Contents
1. [Abstract](#abstract)
2. [Features](#features)
3. [Hardware & Software Requirements](#hardware--software-requirements)
4. [Quickstart](#quickstart)
    - [CompactRIO / LabVIEW](#compactrio--labview)
    - [Raspberry Pi Version](#raspberry-pi-version)
5. [Folder Structure](#folder-structure)
6. [Data & Logging](#data--logging)
7. [Results & Comparison](#results--comparison)
8. [Reproducing Plots](#reproducing-plots)
9. [License](#license)
10. [Acknowledgements](#acknowledgements)
11. [Authors & Contact](#authors--contact)

---

## 📌 Abstract
This project implements a **Smart Spindle Health Monitoring System** that:
- Automatically runs a user-defined **warm-up cycle** for thermal stabilization.
- Monitors **vibration spectra in real-time** using FFT.
- Logs data **only at target RPMs** where faults are more likely to occur.
- Supports **automated triggering** for data acquisition and storage.

Two versions are provided:
1. **Industrial-grade** NI CompactRIO + LabVIEW system with IEPE accelerometer.
2. **Low-cost** Raspberry Pi–based alternative using LM317 constant current source, MCP3208 ADC, and Python for processing.

---

## 🚀 Features
- **Warm-up & Actual Cycle Automation** — one-click spindle startup, warm-up, and analysis.
- **Real-Time FFT Analysis** — detect peaks for imbalance, misalignment, and bearing wear.
- **Automated Triggering** — logs only at relevant spindle speeds.
- **Dual Platform** — high-precision LabVIEW & cost-effective Raspberry Pi setup.
- **Adaptable Design** — easily configurable for other spindles/machines.
- **Data Storage** — saves in `.tdms` (LabVIEW) or `.csv` (Raspberry Pi) for further processing.

---

## 🛠 Hardware & Software Requirements

### **CompactRIO / LabVIEW Version**
- NI CompactRIO 9040
- NI 9234 – IEPE vibration signal acquisition
- NI 9263 – Analog voltage output (VFD speed control)
- NI 9375 – Digital I/O (spindle ON/OFF, direction)
- Industrial IEPE accelerometer
- Variable Frequency Drive (VFD)
- LabVIEW with FPGA & RT modules

### **Raspberry Pi Version**
- Raspberry Pi 3/4
- MCP3208 10-bit ADC
- LM317-based constant current source
- TL072 Op-Amp (buffer)
- Passive components (resistors, capacitors)
- Python 3 with `numpy`, `matplotlib`, `spidev`

---

## ⚡ Quickstart

### **CompactRIO / LabVIEW**
1. Open LabVIEW and load the project files from `labview/VIs/` or drag a VI snippet from `labview/snippets/` into LabVIEW.
2. Connect the CompactRIO and configure the modules (NI 9234, 9263, 9375) in the chassis.
3. Deploy `FPGA.vi` to FPGA and `RT.vi` to the real-time processor.
4. Launch the PC UI (`PC_VI_BLOCK-DIAGRAM.vi`) for control and monitoring.
5. Click **Start Cycle** to run warm-up and actual test cycles automatically.

![LabVIEW FPGA Block Diagram](media/FPGA_VI.png)  
![LabVIEW PC Control Block Diagram](media/PC_VI_BLOCK-DIAGRAM.png)

---

### **Raspberry Pi Version**
1. Enable SPI on Raspberry Pi:
   ```bash
   sudo raspi-config -->
![banner](media/User-Interface.png)

# Smart Spindle Health Monitoring System
**Industrial-grade LabVIEW solution and cost-effective Raspberry Pi alternative for real-time vibration-based spindle health monitoring.**

---

## 📌 Overview
This project combines **high-precision NI CompactRIO + LabVIEW** control with a **low-cost Raspberry Pi system** to monitor spindle health, detect faults, and enable predictive maintenance.

Key Features:
- Real-time **FFT analysis** and **automated triggering**.
- **Thermal warm-up cycle** before data collection.
- **Industrial + low-cost platforms** for flexibility.
- **Accurate fault detection** for imbalance, misalignment, and bearing wear.

---

## 🖥 System Interface
![LabVIEW User Interface](media/User-Interface.png)

---

## 🔧 System Architecture

**LabVIEW FPGA Block Diagram**  
![LabVIEW FPGA Block Diagram](LabVIEW%20Snippets/FPGA_VI.png)

**LabVIEW PC Control Block Diagram**  
![LabVIEW PC Control Block Diagram](LabVIEW%20Snippets/PC_VI.png)

---

## 📡 Hardware Setup

**Raspberry Pi + Arduino Schematic**  
![Raspberry Pi Arduino Schematic](media/Raspberry_Arduino.png)

**LabVIEW CompactRIO Wiring Diagram** *(PDF in repo)*  
📄 [`schematics/LabVIEW_cRIO.pdf`](schematics/LabVIEW_cRIO.pdf)  

**Raspberry Pi Circuit Diagram** *(PDF in repo)*  
📄 [`schematics/RaspberryPi_Arduino.pdf`](schematics/RaspberryPi_Arduino.pdf)

---

## 📊 Results Showcase

**Benchmarking & Cost Analysis**  
![Benchmarking Cost](results/Benchmarking%20Cost.png)

**Calibrometer Output – LabVIEW**  
![Calibrometer LabVIEW](results/Calibrometer_LabVIEW.png)

**Calibrometer Output – Low-cost System**  
![Calibrometer Cost](results/Calibrometer_Cost.png)

**Frequency Spectrum Example**  
![Frequency Spectrum](results/Frequency-Spectrum.png)

**Spindle Vibration Signal**  
![Spindle Vibration](results/Spindle-Vibration.png)

---

## ⚖️ System Comparison
| Feature | CompactRIO (LabVIEW) | Raspberry Pi |
|---|---|---|
| Max Sampling Rate | 50+ kHz | 25.6 kHz |
| Channels | Multi | Single |
| Accuracy | High | Moderate |
| Cost | High | Low |
| Ideal Use | Industrial | Educational / Low-budget |

---

## 🙏 Acknowledgements
- **Indian Institute of Technology Kanpur**
- **Mentor:** Dr. Mohit Subhash Law

---

## 👨‍💻 Authors
- **Humayun Ahmad**  
- **Chanda Bhavitha Sri**  
- **Jainam Tated**  
