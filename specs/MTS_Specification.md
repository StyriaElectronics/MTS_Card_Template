# 📘 MTS – Modular Test System: Spezifikation

**Version:** 1.1
**Autor:** András Nagy
**Lizenz:** CC BY-NC 4.0
**Stand:** 04.05.2025

---

## 📐 1. Mechanische Abmessungen

### 1.1 Platinengröße

* Gesamtbreite: 159,95 mm
* Gesamthöhe: 100,00 mm
* PCB-Dicke: 1,6 mm

### 1.2 Bohrungen

* 2 Montagelöcher Ø 3,2 mm
* Position:

  * Links unten: 6 mm von links / 6 mm von unten
  * Rechts oben: 6 mm von rechts / 5,5 mm von oben

### 1.3 Keepout-Zonen

* 5 mm an Ober- und Unterkante (für Führungsschienen)

---

## 🔌 2. Steckverbinder

* **Typ:** DIN 41612, Type C (ZB), 2x16 Pins
* **Footprint:** `DIN41612_02x16_ZB`
* **Montageart:** senkrecht an rechter PCB-Kante
* **Leiste:** Stiftleiste auf Modul, Buchse auf CPU-Board

---

## 📍 3. Pinbelegung

| Pin     | Signal        | Beschreibung             |
| ------- | ------------- | ------------------------ |
| a1      | Trigger       | Trigger-Eingang          |
| b1      | CAN\_H        | CAN Bus High             |
| b2      | CAN\_L        | CAN Bus Low              |
| b3      | I2C\_BUS\_SDA | I²C Datenleitung         |
| b4      | I2C\_BUS\_CLK | I²C Taktleitung          |
| a11–a12 | +12 V         | Versorgung +12 V (1 A)   |
| b11–b12 | –12 V         | Versorgung –12 V (0.2 A) |
| a13–a14 | +3.3 V Ext    | Versorgung 3.3 V (0.5 A) |
| a15–a16 | +5 V Ext      | Versorgung 5 V (1 A)     |
| b13–b16 | GND           | Masse                    |

> Nicht belegte Pins können projektspezifisch verwendet werden.

---

## ⚡ 4. Spannungsversorgung

| Spannung | Bereich        | Max. Strom |
| -------- | -------------- | ---------- |
| +12 V    | 11.5–12.5 V    | 1 A        |
| –12 V    | –11.5– –12.5 V | 0.2 A      |
| +3.3 V   | 3.2–3.4 V      | 0.5 A      |
| +5 V     | 4.9–5.2 V      | 1 A        |

> ⚠️ Keine Rückspeisung vom Modul!

---

## 🖥️ 5. Kommunikationsbusse

### 5.1 I²C

* Standard Mode: 100 kHz
* Pullups auf CPU-Board

### 5.2 CAN

* ISO 11898-kompatibel
* galvanisch entkoppelt (optional)
* Terminierung: 120 Ω auf CPU-Board

### 5.3 EtherCAT

* Hochgeschwindigkeits-Echtzeit-Kommunikation
* EtherCAT nach IEC 61158 Standard
* RJ45-Anschluss auf CPU-Board
* Unterstützt Datenraten bis zu 100 Mbit/s
* Dedizierte EtherCAT-Module für schnelle Datenerfassung und Steuerung

---

## 🧩 Modul-Kategorien

| Typ              | Funktion                                                  |
| ---------------- | --------------------------------------------------------- |
| CPU-Board        | zentrale Steuerung (z. B. Raspberry Pi CM4)               |
| IO-Karten        | Relais, Optokoppler, PWM, Digitale Eingänge               |
| DAQ-Karten       | ADC-Karten, DAC-Karten, Sensorinterfaces                  |
| Interfacekarten  | EtherCAT-Slave, CAN-Bus, RS485/Modbus, UART               |
| Leistungs-Karten | DC/DC-Konverter, Lasttreiber, Sicherungs- und Überwachung |
| Wireless-Karten  | Wi-Fi/Bluetooth, LoRa/LPWAN                               |
| Spezialkarten    | Kalibrations-, Multiplexer-, Signalverarbeitungskarten    |

---

## 📄 7. Lizenz

Dieses Projekt steht unter der
[**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**](https://creativecommons.org/licenses/by-nc/4.0/)

**Kommerzielle Nutzung ist ohne separate Lizenz nicht gestattet.**

---

**© 2025 Styria Electronics**
