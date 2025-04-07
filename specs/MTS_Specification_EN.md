# 📘 MTS – Modular Test System: Specification

**Version:** 1.0  
**Author:** Styria Electronics  
**License:** CC BY-NC 4.0  
**Date:** 07.04.2025  

---

## 📐 1. Mechanical Dimensions

### 1.1 PCB Size
- Width: 160.00 mm  
- Height: 100.00 mm  
- PCB Thickness: 1.6 mm  

### 1.2 Mounting Holes
- 2 optional mounting holes Ø 3.2 mm
- Position:
  - Bottom-left: 6 mm from left / 6 mm from bottom
  - Top-right: 6 mm from right / 5.5 mm from top

### 1.3 Keepout Zones
- 5 mm top and bottom edge (for guide rails)

---

## 🔌 2. Connector

- **Type:** DIN 41612, Type C (ZB), 2x16 pins  
- **Footprint:** `DIN41612_02x16_ZB`  
- **Mounting:** Vertical, right PCB edge  
- **Orientation:** Male on module, female on CPU board

---

## 📍 3. Pinout

| Pin | Signal        | Description              |
|-----|---------------|--------------------------|
| a1  | Triger        | Trigger input            |
| b1  | CAN_H         | CAN bus high             |
| b2  | CAN_L         | CAN bus low              |
| b3  | I2C_BUS_SDA   | I²C data line            |
| b4  | I2C_BUS_CLK   | I²C clock line           |
| a11–a12 | +12 V     | +12 V power (1 A max)    |
| b11–b12 | –12 V     | –12 V power (0.2 A max)  |
| a13–a14 | +3.3 V Ext| 3.3 V ext. power (0.5 A) |
| a15–a16 | +5 V Ext  | 5 V ext. power (1 A)     |
| b13–b16 | GND       | Ground                   |

> Unused pins can be used for project-specific signals.

---

## ⚡ 4. Power Supply

| Voltage | Range       | Max Current |
|---------|-------------|-------------|
| +12 V   | 11.5–12.5 V | 1 A         |
| –12 V   | –11.5– –12.5 V | 0.2 A     |
| +3.3 V  | 3.2–3.4 V   | 0.5 A       |
| +5 V    | 4.9–5.2 V   | 1 A         |

> ⚠️ No backfeeding from module side allowed!

---

## 🖥️ 5. Communication Buses

### 5.1 I²C
- Standard mode: 100 kHz
- Pull-up resistors located on the CPU board

### 5.2 CAN
- ISO 11898 compatible
- Optional galvanic isolation
- Termination: 120 Ω on CPU board

---

## 🧩 6. Module Types

| Type             | Description                               |
|------------------|-------------------------------------------|
| CPU Board        | Central controller (e.g. CM4)             |
| IO Cards         | Digital/analog I/O (relays, PWM, etc.)    |
| DAQ Cards        | Data acquisition (ADC/DAC)                |
| Interface Cards  | CAN, UART, USB, etc.                      |

---

## 📄 7. License

This project is licensed under the  
[**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**](https://creativecommons.org/licenses/by-nc/4.0/)

**Commercial use is not permitted without a separate license.**

---

**© 2025 Styria Electronics András Nagy**
