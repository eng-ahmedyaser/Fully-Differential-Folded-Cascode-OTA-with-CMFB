# Fully-Differential-Folded-Cascode-OTA-with-CMFB

## Overview
This repository contains the design and simulation results of an Operational Amplifier (Op-Amp) implemented in **0.18 µm (180 nm) CMOS technology**. The design was systematically optimized to meet stringent closed-loop performance metrics using modern analog design methodologies.

## Methodology & Tools
* **Design Methodology:** The circuit was designed utilizing the **$g_m/I_D$ design methodology**, ensuring optimal sizing of transistors for a given power and bandwidth budget without relying on tedious trial-and-error iterations.
* **EDA Tools:** Schematic capture, testbench setup, and circuit simulations (AC, DC, Transient, Stability) were performed using **Cadence Virtuoso**.
* **Optimization & Analysis:** Extensive use of the **Analog Designer's Toolbox (ADT)** facilitated the rapid extraction of device lookup tables and the implementation of the $g_m/I_D$ flow.

## Acknowledgments
I would like to extend my sincere gratitude to **Dr. Hesham Omran** for his invaluable guidance and support throughout this project. His course, *"Systematic Analog Design Using the gm/Id Design Methodology"*, along with his insights and remarkable **Analog Designer's Toolbox (ADT)**, were crucial in achieving these results. Additionally, his paper, [Optimum Split Ratio for Folded Cascode OTA Bias Current: A Qualitative and Quantitative Study](https://www.researchgate.net/publication/339758769_Optimum_Split_Ratio_for_Folded_Cascode_OTA_Bias_Current_A_Qualitative_and_Quantitative_Study), served as an essential reference for analysis and design optimization.

## Achieved Specifications (Simulation Results)

The following table summarizes the target requirements versus the achieved performance in the Cadence simulation environment.

| Parameter | Required | Achieved |
| :--- | :--- | :--- |
| **Technology** | - | 0.18 µm |
| **Supply Voltage ($V_{DD}$)** | - | 2.5 V |
| **Closed Loop Gain ($A_{v_{CL}}$)** | 2 | 1.998 |
| **Phase Margin (at required $A_{v_{CL}}$)** | $\ge 70^\circ$ | $88.64^\circ$ |
| **CMIR - low** | $\le 0$ | $-505$ mV |
| **CMIR - high** | $\ge 1$ V | $1.46$ V |
| **Differential Output Swing** | 1.2 V peak-to-peak | 1.9 V peak-to-peak |
| **DC Loop Gain (LG)** | 60 dB | 60.91 dB |
| **Closed Loop settling time ($t_s$)** | 100 ns | 99.38 ns |
| **Total Current Consumption ($I_{total}$)**| Reasonable | 63.74 µA |
| **Area** | Reasonable | 159.77 µm² |
| **FOM** $\left(\frac{GBW_{CL}}{Area \times I_{total}}\right)$| As High as possible| 0.001731126 MHz/(µA·µm²) |
| **Chip Power Consumption** ($V_{DD} \times I_{total}$) | Reasonable | 159.35 µW |

