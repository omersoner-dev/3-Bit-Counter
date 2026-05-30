# 3-Bit Asynchronous Up-Counter with Adjustable Clock and Reset

This repository contains the schematic design of a 3-bit asynchronous (ripple) up-counter developed using KiCad. The system utilizes sequential digital logic components to achieve stable binary counting from 000 to 111 (0 to 7 in decimal) with real-time frequency control and synchronous/asynchronous system reset capabilities.

## 🚀 Key Features

- **Sequential Logic Core:** Implemented using negative-edge triggered J-K Flip-Flops configured in toggle mode.
- **Adjustable Clock Source:** Driven by an NE555 timer configured in astable multivibrator mode, offering precise frequency tuning via a potentiometer.
- **Visual Indicators:** Dual-output monitoring interface featuring 3-bit binary status LEDs and a decoded 7-segment display output.
- **System Reset:** Active-low reset mechanism equipped with a debounce/pull-up resistor configuration for instant state initialization ($000$).
- **Noise Immunity:** Integrated decoupling capacitors on the $V_{CC}$ rail and the NE555 control pin to minimize signal degradation and voltage ripples.

## 📊 Technical Specifications

- **Operating Voltage ($V_{CC}$):** 5.0 V DC (Standard TTL Logic Levels)
- **Counting Range:** $000_2$ to $111_2$ ($0_{10}$ to $7_{10}$)
- **Max Time Delay per Step:** Approximately 2.0 seconds (Configured via 30kΩ Potentiometer and 47µF Capacitor)

## 📐 Circuit Schematic

[View Circuit Schematic PDF](3 Bit Counter.pdf)

---

## 🛠️ Bill of Materials (BOM)

| Qty | Component Reference | Description | Package Type |
| :---: | :--- | :--- | :---: |
| 2 | 74LS73 | Dual J-K Flip-Flops with Clear | DIP-14 |
| 1 | 74LS48 | BCD to 7-Segment Decoder/Driver | DIP-16 |
| 1 | NE555 | General Purpose Timer | DIP-8 |
| 1 | 7-Segment Display | Common Cathode Display | DIP |
| 1 | Potentiometer | 30kΩ Linear Potentiometer | Through-Hole |
| 1 | Capacitor | 47µF Electrolytic Capacitor (Polarized) | Radial |
| 1 | Capacitor | 100µF Electrolytic Capacitor (Power Rail Bypass) | Radial |
| 1 | Capacitor | 100nF Ceramic Capacitor (Control Voltage Decoupling) | Disc |
| 3 | LED | Standard Status Indicator LEDs | 5mm THT |
| 10 | Resistor | 330Ω Current Limiting Resistors (LEDs & Display) | Axial |
| 1 | Resistor | 1kΩ Timing Resistor | Axial |
| 1 | Resistor | 10kΩ Pull-Up Resistor (Reset Circuit) | Axial |
| 1 | Tactile Switch | Push-Button (Momentary Switch) | 4-pin THT |
