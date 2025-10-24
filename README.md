# ⚡ EchoVolt: Ultrasound Signal Detection and Reconstruction

**EchoVolt** is a complete signal processing project that demonstrates the full cycle of **data acquisition, digital encoding, and analog reconstruction** — bridging physical sensing and embedded systems.

---

## 🎯 Project Overview

This project converts a **physical distance measurement** from an **ultrasonic sensor** into an analog voltage using an **Arduino Uno**.  
The analog signal then goes through a **custom 3-bit Flash-type Analog-to-Digital Converter (ADC)**, whose output bits control a **servo-driven switch** to produce discrete voltage levels.  
Finally, an **R-2R ladder Digital-to-Analog Converter (DAC)** reconstructs the original analog voltage, which is validated by a voltmeter reading.

---

## ⚙️ System Workflow

```mermaid
flowchart LR
    A[Ultrasonic Sensor] --> B[Arduino Uno (Analog Voltage Out)]
    B --> C[3-bit Flash ADC]
    C --> D[SG90 Servo Motor (Switch Control)]
    D --> E[R-2R Ladder DAC]
    E --> F[Voltmeter (Output Measurement)]
