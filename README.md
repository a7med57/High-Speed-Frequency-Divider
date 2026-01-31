# High-Speed CMOS Frequency Divider (65nm)

**Course:** Digital Integrated Circuits (EECG271)
**Technology:** 65nm CMOS PDK
**Tools:** Cadence Virtuoso, ADE L/XL

## Project Overview
This project involves the design and simulation of a high-speed **Divide-by-2 Frequency Divider** capable of operating at **2 GHz**. The goal was to optimize the circuit for **Power-Delay Product (PDP)** and maximum operating frequency using the **True Single-Phase Clock (TSPC)** logic style.


*Figure 1: Transistor-level schematic of the TSPC Divide-by-2 circuit.*

## Design Specifications

| Parameter | Specification | Achieved Result |
| :--- | :--- | :--- |
| **Technology Node** | 65 nm | 65 nm |
| **Supply Voltage** | 1.0 V - 1.2 V | 1.2 V |
| **Input Frequency** | 2.0 GHz | **2.5 GHz (Max)** |
| **Logic Style** | TSPC / CML | **TSPC (True Single Phase Clock)** |
| **Duty Cycle** | ~50% | **48%** |

## Circuit Architecture
The design utilizes a **TSPC (True Single-Phase Clock)** D-Flip Flop topology connected in a negative feedback loop ($\bar{Q}$ to $D$). This architecture was chosen over Static CMOS and CML for its superior high-speed performance and lower clock load.

### Key Features
* **Reduced Transistor Count:** 9-transistor TSPC topology to minimize parasitic capacitance.
* **Low Power:** Dynamic logic reduces static power consumption compared to CML.
* **High Speed:** Optimized sizing ($W/L$) to minimize rise/fall times at the 2GHz target.

## Simulation Results

### 1. Transient Response (@ 2GHz)
The circuit successfully divides the 2GHz input clock to a 1GHz output with full rail-to-rail swing.


### 2. Power Consumption
* **Average Power:** ~45 $\mu W$ @ 2GHz
* **Figure of Merit (FoM):** Optimized for $\frac{\text{Power}}{\text{Freq}}$.



## Documentation
For full transistor sizing, propagation delay analysis, and trade-offs, please refer to the [Project Report](High-Speed-Frequency-Divider
/docs/Frequency Divider Project.pdf).
