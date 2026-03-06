---
layout: default
title: Learning Plan
---
# Learning Plan 

### Returning to Science

After burning out on math and science as a kid—because, spoiler, things are supposed to be hard—I’m back, driven by curiosity and the joy of figuring things out. Amateur radio grabbed my attention after reading *Remembrance of Earth’s Past* by Liu Cixin and listening to *Daniel and Kelly’s Extraordinary Universe*. Both reignited my fascination with how the universe works, and ham radio lets me explore that curiosity hands-on through the electromagnetic spectrum.

### Operating and Experimenting

Progress is uneven. Most of my free time is on the train or late at night, so I won’t always be building or operating. Even small experiments, though, keep me engaged.  

I’m starting as a Technician with a few months of experience and working toward General and Amateur Extra. My goal isn’t just passing exams; I want to understand the material behind them. I'll be exploring antennas, circuits, operating, and building a small station. That includes trial-and-error projects like a 2 m Yagi or a 40 m dipole, logging QSOs on BrandMeister and eventually on HF.

### Theory and Math

I’ve started with Bertrand’s *Advanced Radio Theory Handbook* to build a foundation in electronics and RF. Eventually, I want to reconnect with the math, from calculus to Maxwell’s equations, so the theory aligns with what I hear and build on the air. Understanding the equations behind what I’m doing will make operating and building immensely satisfying. The goal is to connect theory and practice.

### Connected Interests

Amateur radio also fuels other interests: building and hosting this site, tinkering with Raspberry Pi projects, and experimenting with Python for small data analyses. This site serves as my lab notebook, documenting experiments, ideas, and rabbit holes as they unfold.



# Experimental RF Learning Workflow

This workflow shows how theory, math, Python, and hardware interact in a modular experimental base station setup. The focus is on exploration, measurement, and iteration rather than casual chatting.

---

## **1. Theory Layer (Maxwell & Circuit Concepts)**

- Study fundamental electromagnetic principles:
  - Gauss’s Law → capacitor/voltage experiments
  - Faraday’s Law → coil/induction tests
  - Ampère’s Law → current/magnetic field exploration
  - Wave Equations → RF propagation & antenna behavior
- Design experiments and predict expected outcomes before building.

---

## **2. Math Layer**

- Use formulas and calculations to design circuits:
  - Resonant frequency: \( f = \frac{1}{2\pi\sqrt{LC}} \)
  - Impedance, voltage dividers, filter responses
  - Gain and SNR calculations
  - Fourier analysis for signal decomposition
- Compare predicted values with experimental measurements.

---

## **3. Python Layer**

- Data acquisition and analysis:
  - Read Arduino sensor outputs via `pyserial`
  - Capture SDR signals for spectrum analysis
  - Plot waveforms, FFTs, and filter responses (`matplotlib`, `numpy`, `scipy`)
- Simulation and experiment planning:
  - Model filters, antenna responses, and signal propagation
  - Generate test waveforms to feed into Arduino/DDS modules
- Automate experiments and log results for iteration.

---

## **4. Hardware Layer**

### **A. Control**
- **Arduino Uno/Nano**
  - Drives DDS modules (Si5351, AD9833)
  - Controls switches, sensors, and circuits
  - Handles timing-critical operations
- **Raspberry Pi**
  - Interfaces with SDRs
  - Runs analysis, visualization, and logging scripts
  - Optional GUI for experiment control

### **B. Signal Generation**
- **Si5351 Module** → HF/VHF square waves
- **AD9833 Module** → precise sine/triangle signals
- Optional analog signal generator for lab measurements

### **C. RF Front-End**
- Experimental transceivers (QRP rigs, modules like NRF24L01 or HC‑12)
- Filters, amplifiers, matching networks
- Antennas (dipoles, loops, verticals)
- Dummy loads for safe testing

### **D. Measurement**
- SDR (RTL-SDR, HackRF/LimeSDR)
- Oscilloscope / multimeter
- Frequency counter (optional)

### **E. Optional Benchmark / Real-World Reference**
- IC‑7300 HF Transceiver
  - Compare DIY signals with real-world HF
  - Safe low-power testing and propagation observation
  - Control via CAT/USB for logging and experiment integration

---

## **5. Workflow: Experiment Cycle**

1. **Theory → Prediction**  
   - Use Maxwell’s equations and math to calculate expected behavior.
2. **Design → Build**  
   - Assemble circuits on breadboard; program DDS/Arduino to generate signals.
3. **Measure → Observe**  
   - Capture signals with SDR, Arduino ADC, or oscilloscope.
4. **Analyze → Compare**  
   - Process measurements in Python; compare against theoretical predictions.
5. **Iterate → Refine**  
   - Adjust components, waveforms, or antennas and repeat cycle.
6. **Optional Benchmark**  
   - Use IC‑7300 or other HF rig to verify real-world propagation or signal quality.

---

### 💡 Notes

- Every layer is **interconnected**: Theory informs design, math predicts results, Python analyzes data, and hardware implements experiments.
- This workflow supports **exploration across all frequencies, modulation schemes, and circuit types**.
- Modular approach allows **incremental growth**: start small (Arduino + DDS), then expand (SDR + Pi), then integrate real HF rig for real-world verification.
