# ⚡ Two-Stage Op-Amp Design — Analog Circuits & Sensor Systems

Design and simulation of a two-stage CMOS operational amplifier using LTSpice, developed as part of the Analog Circuits and Sensor Systems course at the University of Bologna. All target specifications were met and exceeded through systematic transistor sizing and circuit simulation.

---

## 📌 Project Overview

This project involves the full design flow of a two-stage CMOS op-amp — from hand calculations and transistor sizing to circuit simulation and performance verification in LTSpice. The design targets high differential gain, stable phase margin, and low noise, making it suitable for precision sensor signal conditioning applications.

---

## 🎯 Target vs Achieved Specifications

| Parameter | Target | Achieved |
|---|---|---|
| Supply Voltage (VDD/VSS) | 2.5 / -2.5 V | 2.5 / -2.5 V ✅ |
| Slew Rate | ±5 V/µs | ±13 V/µs ✅ |
| Max Input Common Mode | 2.1 V | 2.2 V ✅ |
| Min Input Common Mode | -1.3 V | -1.8 V ✅ |
| Max Output Swing | 2.2 V | 2.5 V ✅ |
| Min Output Swing | -2.2 V | -2.5 V ✅ |
| Gain Bandwidth | 5 MHz | 7 MHz ✅ |
| Differential Gain | > 80 dB | 94 dB ✅ |
| Phase Margin | > 60° | 83° ✅ |

> All specifications exceeded target values.

---

## 🛠️ Design Parameters

| Parameter | Value |
|---|---|
| Load Capacitor (CL) | 5 pF |
| Noise Voltage | 38 nV/√Hz |
| Gain Bandwidth (ω) | 31.415 Mrad/sec |
| Vtn / Vtp | 0.71 / -0.901 V |
| β'n / β'p | 182e-6 / 41.5e-6 |

---

## ⚙️ Design Procedure

The design followed a structured transistor sizing methodology:

1. **Compensation capacitance Cc** — calculated from noise and slew rate constraints
2. **Transistor M6** — sized from output swing and phase margin requirements
3. **Bias currents** — I5 derived from slew rate; I1–I4 set as I5/2
4. **Input differential pair (M1, M2)** — sized from gain-bandwidth and overdrive voltage
5. **Current mirror (M3, M4)** — sized for perfect balance (VSG6 = VSG4 = VSG3)
6. **Output stage (M7)** — sized relative to M5 and compensation capacitor
7. **Biasing network (M8–M14)** — designed for stable operating point
8. **Compensation resistor** — replaced with transistor M9 for integration

All transistors verified in saturation via `.op` simulation before full circuit analysis.

---

## 🔬 Simulations Performed

- **AC Analysis** — Gain Bandwidth and Phase Margin verification
- **Noise Analysis** — Input-referred noise voltage across frequency
- **DC Sweep (CMRR)** — Common Mode Rejection Ratio measurement
- **Transient Analysis (Slew Rate)** — Rise/fall time characterisation
- **Output Swing (OPSWING)** — Maximum and minimum output voltage range

---

## 🧰 Tools Used

- **LTSpice** — Circuit schematic, simulation, and analysis
- **Hand Calculations** — Transistor sizing using analytical design equations

---

## 📁 Repository Structure

```
├── schematic/          # LTSpice schematic files (.asc)
├── simulations/        # Simulation result files (.raw)
├── results/            # Plots: CMRR, gain-bandwidth, noise, slew rate, phase margin
├── report/             # Full design report (PDF)
└── README.md
```

---

## 👩‍💻 Author

**Wajeeha Kazmi**
MSc Electronics Engineering for Intelligent Systems, Big Data & IoT
University of Bologna, Italy
[LinkedIn](https://www.linkedin.com/in/wajeeha-kazmi)
