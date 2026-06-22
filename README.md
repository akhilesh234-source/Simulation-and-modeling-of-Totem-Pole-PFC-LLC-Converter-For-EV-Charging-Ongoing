# Design and Control of Full Bridge LLC Resonant Converter using DSP and FPGA

[![MATLAB/Simulink](https://img.shields.io/badge/MATLAB-Simulink-orange.svg)](https://www.mathworks.com/products/simulink.html)
[![FPGA](https://img.shields.io/badge/FPGA-Nexys%20A7--100T-blue.svg)](https://digilent.com/reference/programmable-logic/nexys-a7/start)
[![DSP](https://img.shields.io/badge/DSP-TMS320F28379D-green.svg)](https://www.ti.com/product/TMS320F28379D)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📋 Overview

This repository presents a comprehensive investigation into the design, modeling, and real-time validation of advanced power converter topologies for high-efficiency electric vehicle (EV) charging systems. The work encompasses three interconnected studies:

1. **Market-Driven Survey**: Analysis of contemporary EV architectures and competitive landscape, identifying key trends in fast-charging infrastructure and converter technology adoption across Indian and global markets.

2. **Systematic Simulation**: Comparative analysis of industry-standard Totem-Pole Power Factor Correction (PFC) and Full-Bridge LLC resonant converter topologies in MATLAB/Simulink, evaluating performance metrics including efficiency, transient response, and harmonic distortion.

3. **Real-Time Validation**: FPGA and DSP-based hardware validation with discrete-time digital controllers, demonstrating seamless integration between simulation environments and embedded implementations.

## ⚡ Key Features

- **Two-Stage EV Charger Architecture**: Totem-Pole PFC + Full-Bridge LLC Resonant Converter
- **Power Rating**: 7.7 kW (400 V DC-link, 400 V output)
- **Soft-Switching**: Primary-side Zero Voltage Switching (ZVS) and secondary-side Zero Current Switching (ZCS)
- **Digital Control**: Pulse Frequency Modulation (PFM) with digital PI controller
- **Control Platforms**: Nexys A7-100T FPGA and TMS320F28379D DSP
- **Modeling**: Extended Describing Function (EDF)-based small-signal modeling
- **Hardware Prototype**: 400 W validation with custom magnetic components

## 📊 System Architecture
<img width="968" height="206" alt="image" src="https://github.com/user-attachments/assets/d0c5b7f5-99c3-4cbc-ae57-9fb97e240742" />



## 🎯 Research Contributions

### 1. Power Converter Design
- Designed Totem-Pole PFC converter with boost inductance (180 μH) and DC-link capacitance (7660 μF)
- Designed Full-Bridge LLC resonant converter with resonant tank parameters:
  - Resonant Inductance (Lᵣ): 16.07 μH
  - Resonant Capacitance (Cᵣ): 630 nF
  - Magnetizing Inductance (Lₘ): 80.35 μH
  - Quality Factor (Q): 0.3
  - Inductance Ratio (m): 6

### 2. Control System Development
- Derived EDF-based small-signal model (7th order state-space)
- Designed digital PI controller with:
  - Crossover Frequency: 800 Hz
  - Phase Margin: 60°
  - Gain Margin: 6.96 dB
- Implemented PFM-based output voltage regulation
- Developed anti-windup protection for robust performance

### 3. Hardware Implementation
- Custom high-frequency transformer (EE100/60/28, N87 ferrite, 2.8 mH)
- Custom resonant inductor (EE70/33/32, 306 μH, 0.5 mm air-gap)
- Isolated gate driver circuitry
- Signal conditioning for voltage/current sensing

### 4. Platform Validation
- Nexys A7-100T FPGA: Open-loop pulse generation and validation
- TMS320F28379D DSP: Open-loop and closed-loop control implementation
- Identical performance across both platforms confirming design robustness

