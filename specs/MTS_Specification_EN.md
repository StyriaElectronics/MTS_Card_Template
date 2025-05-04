# 📘 MTS – Modular Test System: Specification

**Version:** 1.1
**Author:** András Nagy
**License:** CC BY-NC 4.0
**Date:** 04.05.2025

---

## 📐 1. Mechanical Dimensions

### 1.1 PCB Size

* Total width: 159.95 mm
* Total height: 100.00 mm
* PCB thickness: 1.6 mm

### 1.2 Mounting Holes

* 2 mounting holes Ø 3.2 mm
* Positions:

  * Bottom left: 6 mm from left / 6 mm from bottom
  * Top right: 6 mm from right / 5.5 mm from top

### 1.3 Keepout Zones

* 5 mm at top and bottom edges (for guide rails)

---

## 🔌 2. Connectors

* **Type:** DIN 41612, Type C (ZB), 2x16 Pins
* **Footprint:** `DIN41612_02x16_ZB`
* **Mounting:** vertical at the right PCB edge
* **Connector:** Pin header on module, socket on CPU board

---

## 📍 3. Pin Assignment

| Pin     | Signal        | Description          |
| ------- | ------------- | -------------------- |
| a1      | Trigger       | Trigger input        |
| b1      | CAN\_H        | CAN Bus High         |
| b2      | CAN\_L        | CAN Bus Low          |
| b3      | I2C\_BUS\_SDA | I²C Data line        |
| b4      | I2C\_BUS\_CLK | I²C Clock line       |
| a11–a12 | +12 V         | Supply +12 V (1 A)   |
| b11–b12 | –12 V         | Supply –12 V (0.2 A) |
| a13–a14 | +3.3 V Ext    | Supply 3.3 V (0.5 A) |
| a15–a16 | +5 V Ext      | Supply 5 V (1 A)     |
| b13–b16 | GND           | Ground               |

> Unassigned pins may be used for specific projects.

---

## ⚡ 4. Power Supply

| Voltage | Range          | Max. Current |
| ------- | -------------- | ------------ |
| +12 V   | 11.5–12.5 V    | 1 A          |
| –12 V   | –11.5– –12.5 V | 0.2 A        |
| +3.3 V  | 3.2–3.4 V      | 0.5 A        |
| +5 V    | 4.9–5.2 V      | 1 A          |

> ⚠️ No back-feeding from modules!

---

## 🖥️ 5. Communication Buses

### 5.1 I²C

* Standard Mode: 100 kHz
* Pull-up resistors on CPU board

### 5.2 CAN

* ISO 11898 compatible
* Galvanic isolation (optional)
* Termination: 120 Ω on CPU board

### 5.3 EtherCAT

* High-speed real-time communication
* EtherCAT according to IEC 61158 standard
* RJ45 connector on CPU board
* Supports data rates up to 100 Mbit/s
* Dedicated EtherCAT modules for fast data acquisition and control

---

## 🧩 Module Categories

| Type            | Function                                                  |
| --------------- | --------------------------------------------------------- |
| CPU board       | Central control unit (e.g., Raspberry Pi CM4)             |
| IO cards        | Relays, Optocouplers, PWM, Digital Inputs                 |
| DAQ cards       | ADC cards, DAC cards, Sensor interfaces                   |
| Interface cards | EtherCAT Slave, CAN bus, RS485/Modbus, UART               |
| Power cards     | DC/DC converters, Load drivers, Fuse and monitoring cards |
| Wireless cards  | Wi-Fi/Bluetooth, LoRa/LPWAN                               |
| Special cards   | Calibration, Multiplexer, Signal processing cards         |

---

## 📄 7. License

This project is licensed under
[**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**](https://creativecommons.org/licenses/by-nc/4.0/)

**Commercial use requires a separate license agreement.**

---

**© 2025 Styria Electronics**
