# SOLAR-POWERD-ELECTRIC-FENCE-CIRCUIT
A fully custom-built Solar Powered Electric Fence Circuit designed ECE project team. The system uses a solar panel to charge a 12V battery via an LM317L regulator and generates controlled high-voltage pulses using a CD4047 astable multivibrator (f = 46–58 Hz). IRF3205 MOSFETs drive a step-up transformer to deliver electric pulses along the fence.

#📘 Solar Powered Electric Fence Circuit

This repository contains a fully custom-built Solar Powered Electric Fence Circuit, including schematics, PCB layouts, timing calculations, and supporting documentation. The system uses solar energy to charge a 12V battery and generate controlled high-voltage pulses suitable for agricultural and perimeter protection.

🔧 System Overview
1. Solar Charging Stage

Solar panel input with diode protection

LM317L adjustable regulator for controlled battery charging

12V, 7Ah battery for continuous operation

2. Pulse Generation (CD4047 Astable Multivibrator)

Configured in astable mode using:

R = 390 kΩ + 0–100 kΩ variable resistor

C = 10 nF

Formula:

𝑇
=
4.4
𝑅
𝐶
T=4.4RC

Pulse characteristics:

Time Period (T): 17–22 ms

Frequency (f): 46–58 Hz

3. MOSFET Switching Stage

High-current IRF3205 N-channel MOSFETs

Efficient low-loss switching for the transformer

Handles rapid repetitive pulse loads

4. High-Voltage Output Stage

Step-up transformer generates intermittent high-voltage pulses

Safe, short-duration shocks suitable for fencing applications

5. Indicators & Protection

LEDs for power, charging, and pulse output

Schottky diodes for reverse and surge protection

Fuses and optimized PCB routing for safety

📐 Design Features

Fully custom schematics and PCB design

Optimized for high-current pulse switching

Segmented boards for charging, control, and HV output

Suitable for long-term outdoor, off-grid operation

📁 Repository Contents
/hardware
   /schematics
   /pcb

/docs
   timing_calculation_cd4047.md
   project_report.pdf

/media
   pcb_3d_views/
   board_layouts/

🧮 CD4047 Timing Calculation (Summary)

Given:

R = 390 kΩ → 490 kΩ

C = 10 nF

𝑇
min
⁡
≈
17.16
 ms
,
𝑓
max
⁡
≈
58
 Hz
T
min
	​

≈17.16 ms,f
max
	​

≈58 Hz
𝑇
max
⁡
≈
21.56
 ms
,
𝑓
min
⁡
≈
46
 Hz
T
max
	​

≈21.56 ms,f
min
	​

≈46 Hz

Final pulse characteristics:

Period: 17–22 ms

Frequency: 46–58 Hz

🌾 Applications

Agricultural field protection

Livestock fencing

Wildlife deterrence

Off-grid electric barrier systems
