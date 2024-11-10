# 2:1 Multiplexer Design: Schematic to GDSII using GPDK90 in Cadence

This repository contains the complete design flow for a 2:1 Multiplexer (MUX), starting from schematic creation to GDSII generation, using Cadence tools with the GPDK90 process library. A 2:1 multiplexer is a fundamental digital circuit that selects one of two inputs to pass through to the output based on a control signal. This project covers schematic design, layout, design rule checks (DRC), layout versus schematic checks (LVS), and RC extraction.

## Project Overview

### 2:1 Multiplexer: Definition and Truth Table
A 2:1 multiplexer takes two input signals (A and B) and a control signal (S) to determine which input is forwarded to the output.

**Truth Table:**
| Input D1 | Input D0 | Select (S) | Output (Y) |
|---------|---------|------------|------------|
|    0    |    0    |     0      |     0      |
|    0    |    1    |     0      |     0      |
|    1    |    0    |     0      |     1      |
|    1    |    1    |     0      |     1      |
|    0    |    0    |     1      |     0      |
|    0    |    1    |     1      |     1      |
|    1    |    0    |     1      |     0      |
|    1    |    1    |     1      |     1      |

### Design Flow
This project follows a standard ASIC design flow for digital circuits:
1. **Schematic Creation**
2. **Symbol and Testbench Setup**
3. **Pre-Layout Simulation**
4. **Layout Creation (DRC and LVS checks)**
5. **Post-Layout Simulation**
6. **RC Extraction**
7. **GDSII Generation**

---

## Detailed Process and Results

### 1. Schematic Creation
The initial schematic of the 2:1 MUX was created using GPDK90 in Cadence. This schematic forms the base for further simulations and layout design.

**Schematic Diagram:**

### 2. Symbol and Testbench Creation
A symbol view was generated, and a testbench was set up to verify functionality through transient and delay analysis.

### 3. Pre-Layout Simulation Results
Simulations were run to verify the functionality and performance of the 2:1 MUX. Critical parameters, such as propagation delay and power, were analyzed.

### 4. Layout Creation and Verification
The layout was designed using Cadence Virtuoso with GPDK90. Design Rule Check (DRC) and Layout Versus Schematic (LVS) checks were performed to ensure compliance and correctness.

### 5. Post-Layout Simulation Results
Post-layout simulations were conducted to examine performance changes due to parasitic elements.

### 6. RC Extraction
RC extraction was performed to capture parasitic capacitance and resistance, ensuring post-layout simulations reflect realistic circuit behavior.

### 7. GDSII Generation
The final design was exported in GDSII format, a binary format for transferring IC layout data to silicon foundries.

---

## Tools Used
- **Cadence Virtuoso** for Schematic, Layout, and GDSII generation
- **Spectre Simulator** for pre- and post-layout simulations
- **GPDK90**: A generic process design kit based on 90 nm technology

---

## Contributors
- **Ayesha Parveen**  
  B.Tech Electronics Engineering, ZHCET, Aligarh Muslim University (AMU), Aligarh

- **Soliyah Mushtaq**  
  B.Tech Electronics Engineering, ZHCET, Aligarh Muslim University (AMU), Aligarh

---

## Acknowledgements
- We gratefully acknowledge the support from the Chips to Startup (C2S) program, MeitY, Government of India, provided to Aligarh Muslim University, which enabled us to access industry-standard tools and training resources. We also extend our sincere gratitude to our course instructor, Dr. Mohd Wajid, for their invaluable guidance throughout this project. This work is part of the Digital IC Design course in Semester 7 of the B.Tech Electronics Engineering program at Aligarh Muslim University.
