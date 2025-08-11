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
![LabVIEW FPGA Block Diagram](LabVIEW/Snippets/FPGA_VI.png)

**LabVIEW PC Control Block Diagram**  
![LabVIEW PC Control Block Diagram](LabVIEW/Snippets/PC_VI.png)

---

## 📡 Hardware Setup

**Raspberry Pi + Arduino Schematic**  
![Raspberry Pi Arduino Schematic](media/Raspberry_Arduino_Setup.jpg)

**LabVIEW CompactRIO Wiring Diagram** *(PDF in repo)*  
📄 [`schematics/LabVIEW_cRIO.pdf`](schematics/LabVIEW_cRIO.pdf)  

**Raspberry Pi Circuit Diagram** *(PDF in repo)*  
📄 [`schematics/RaspberryPi_Arduino.pdf`](schematics/RaspberryPi_Arduino.pdf)

---

## 📊 Results Showcase

**Benchmarking & Cost Analysis**  
![Benchmarking Cost](results/Benchmarking%20Cost.png)

**Calibrometer Output – LabVIEW**  
![Calibrometer LabVIEW](results/Benchmarking/Calibrometer_LabVIEW_Setup.png)

**Calibrometer Output – Low-cost System**  
![Calibrometer Cost](results/Benchmarking/Calibrometer_Cost-EffectiveSetup.jpg)

**Frequency Spectrum Example**  
![Frequency Spectrum](results/Frequency-Spectrum.png)

**Spindle Vibration Signal**  
![Spindle Vibration](results/Spindle-Vibration-Data.png)

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
