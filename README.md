# Solar Powered Electric Fence Circuit

*A high-voltage, renewable energy-based perimeter security system using CD4047 pulse generation and MOSFET power switching.*

---

## 📘 Overview

This project features a fully custom-built **Solar Powered Electric Fence**, designed to deliver controlled, safe high-voltage pulses for agricultural and perimeter protection. It integrates a solar charging system with a battery backup to ensure 24/7 off-grid operation without reliance on the power grid.

---

## 🏗 System Architecture
┌────────────────────────────┐       ┌────────────────────────────┐
│   Solar Charging Stage     │       │   Pulse Generation Stage   │
│ • 12V Solar Panel          │       │ • CD4047 Multivibrator     │
│ • LM317L Voltage Regulator │◄─────►│ • Adjustable Frequency     │
│ • 12V 7Ah Battery Storage  │       │ • 46 Hz – 58 Hz Range      │
└─────────────┬──────────────┘       └─────────────┬──────────────┘
│                                    │
▼                                    ▼
┌────────────────────────────┐       ┌────────────────────────────┐
│   High-Voltage Stage       │       │      Switching Stage       │
│ • Step-up Transformer      │◄─────►│ • Dual IRF3205 MOSFETs     │
│ • High-Voltage Pulse Out   │       │ • High-Current Handling    │
│ • Safe Deterrent Shocks    │       │ • Low-Loss Power Switching │
└────────────────────────────┘       └────────────────────────────┘
Here is the project description formatted in **Markdown**, ready for your GitHub `README.md` file. I have followed the exact style, hierarchy, and use of tables/boxes from your PWM Modulator example.

```markdown
# Solar Powered Electric Fence Circuit

*A high-voltage, renewable energy-based perimeter security system using CD4047 pulse generation and MOSFET power switching.*

---

## 📘 Overview

This project features a fully custom-built **Solar Powered Electric Fence**, designed to deliver controlled, safe high-voltage pulses for agricultural and perimeter protection. It integrates a solar charging system with a battery backup to ensure 24/7 off-grid operation without reliance on the power grid.

---

## 🏗 System Architecture

```
┌────────────────────────────┐       ┌────────────────────────────┐
│   Solar Charging Stage     │       │   Pulse Generation Stage   │
│ • 12V Solar Panel          │       │ • CD4047 Multivibrator     │
│ • LM317L Voltage Regulator │◄─────►│ • Adjustable Frequency     │
│ • 12V 7Ah Battery Storage  │       │ • 46 Hz – 58 Hz Range      │
└─────────────┬──────────────┘       └─────────────┬──────────────┘
              │                                    │
              ▼                                    ▼
┌────────────────────────────┐       ┌────────────────────────────┐
│   High-Voltage Stage       │       │      Switching Stage       │
│ • Step-up Transformer      │◄─────►│ • Dual IRF3205 MOSFETs     │
│ • High-Voltage Pulse Out   │       │ • High-Current Handling    │
│ • Safe Deterrent Shocks    │       │ • Low-Loss Power Switching │
└────────────────────────────┘       └────────────────────────────┘
```



## ⚙ Working Principle

1. **Energy Harvesting:** The solar panel generates DC power, which is regulated by the **LM317L** to provide a constant charging voltage to the **12V 7Ah Lead-Acid battery**.
2. **Pulse Timing:** A **CD4047 IC** is configured in astable mode to produce a continuous square wave. The frequency is adjustable (**46–58 Hz**) via a variable resistor to fine-tune the deterrent intensity.
3. **Power Switching:** The logic-level signal from the IC drives the gates of two **IRF3205 MOSFETs**. These MOSFETs switch the battery current through the primary winding of the transformer.
4. **Inductive Boost:** The **Step-up Transformer** converts the low-voltage switched DC into high-voltage, short-duration pulses suitable for long-distance fencing wires.

---

## 🧩 Detailed Hardware Information

### 🧮 Pulse Generation (CD4047)
The timing is governed by the RC network connected to the astable multivibrator pins.

| Component | Value | Function |
| :--- | :--- | :--- |
| **Resistor (R)** | 390 kΩ + 100 kΩ Pot | Frequency Tuning |
| **Capacitor (C)** | 10 nF | Timing Constant |
| **Pulse Period (T)** | 17.16 – 21.56 ms | T = 4.4RC |
| **Frequency (f)** | 46 Hz – 58 Hz | Output Pulse Rate |

### 🔋 Power & Switching
| Component | Specification | Role |
| :--- | :--- | :--- |
| **Voltage Regulator** | LM317L | Battery Charge Control |
| **Storage** | 12V, 7Ah Battery | Lead-Acid Energy Storage |
| **Switching MOSFET** | IRF3205 | High-Current Driver ($V_{DSS}=55V$) |
| **Protection** | Schottky Diodes | Reverse Polarity & Surge Protection |

---

## 📐 Design Features

* **Fully Custom Design:** Optimized schematics and PCB layouts specifically for high-current pulse switching.
* **Off-Grid Optimized:** Designed for long-term outdoor operation with minimal maintenance.
* **Safety Integrated:** Intermittent pulse generation ensures shocks are deterrent but safe for livestock and humans.
* **Modular Layout:** Segmented circuit stages for charging, control, and high-voltage output for easier troubleshooting.

---

## 🧪 Verification & Testing

| Test | Condition | Expected Result | Status |
| :--- | :--- | :--- | :--- |
| **Charging** | Solar Input Active | Stable 13.8V to battery | ✅ Pass |
| **Timing (Min)** | Potentiometer at 0Ω | Frequency ≈ 58 Hz | ✅ Pass |
| **Timing (Max)** | Potentiometer at 100kΩ | Frequency ≈ 46 Hz | ✅ Pass |
| **Output** | Fence Connection | Periodic High-Voltage Discharges | ✅ Pass |

---

## 📂 Repository Contents
- `/hardware`: Schematics, PCB layouts, and Gerber fabrication files.
- `/docs`: Timing calculation sheets, safety guidelines, and project report.
- `/media`: 3D PCB renders, circuit diagrams, and board photographs.

---

## 🧠 Learning Outcomes
- Designing **Battery Charging Circuits** with voltage regulation.
- Implementing **Astable Multivibrators** for precise signal timing.
- Managing **High-Voltage switching** and EMI protection in PCB design.
- Integrating **Renewable Energy** into practical security applications.

---

## 🧭 Academic Context
**Institution:** Indian Institute of Information Technology Design and Manufacturing, Kurnool  
**Department:** Electronics and Communication Engineering  
**Academic Year:** 2025–2026  
**Faculty Guidance:** Dr. P. Ranga Babu  

---

## 👨‍🎓 The Team
- **Praneesh** (123EC0043)
- **Chethan** (123EC0049)
- **Abhilash** (123EC0053)
- **Manideep** (523EC0004)
- **Dinesh** (523EC0007)

---

## 🧾 License
**MIT License** Permission is granted to use, modify, and distribute under MIT terms.

---

## ✅ Summary
A robust, solar-powered security solution that demonstrates the practical application of **Power Electronics** and **Analog Design**. The system provides a sustainable, cost-effective deterrent for livestock and perimeter management, verified through rigorous testing and custom PCB fabrication.
```
