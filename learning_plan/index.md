---
layout: default
title: Learning Plan
---
# Learning Plan

# Returning to Science

After burning out on math and science as a kid—because, spoiler, things are supposed to be hard—I’m back, driven by curiosity and the joy of figuring things out. Amateur radio grabbed my attention after reading *Remembrance of Earth’s Past* by Liu Cixin and listening to [Daniel and Kelly’s Extraordinary Universe podcast](https://podcasts.apple.com/us/podcast/daniel-and-kellys-extraordinary-universe/id1436616330). Both reignited my fascination with how the universe works, and ham radio lets me explore that curiosity hands-on through the electromagnetic spectrum.

---

# Operating and Experimenting

Progress is uneven. Most of my free time is on the train or late at night, so I won’t always be building or operating. Even small experiments, though, keep me engaged.

I’m starting as a Technician with a few months of experience and working toward General and Amateur Extra. My goal isn’t just passing exams; I want to understand the material behind them. I’ll be exploring:

- **Antennas**: trial-and-error projects like a 2 m Yagi or a 40 m dipole  
- **Circuits**: Arduino/DDS setups, filters, and RF front ends  
- **Operating and logging**: QSOs on BrandMeister and eventually on HF  
- **Building a small station**: modular and experimental rather than just talking  

---

# Theory and Math

I’ve started with Bertrand’s *Advanced Radio Theory Handbook* to build a foundation in electronics and RF. Eventually, I want to reconnect with the math, from calculus to Maxwell’s equations, so the theory aligns with what I hear and build on the air. Understanding the equations behind my experiments will make operating and building immensely satisfying. The ultimate goal is to **connect theory and practice**.

---

# Connected Interests

Amateur radio also fuels other interests:

- Building and hosting this website as a lab notebook  
- Tinkering with Raspberry Pi projects for experiments  
- Using Python for small data analyses and automation  

This site documents my experiments, ideas, and rabbit holes as they unfold, creating a record of learning and discovery.

---

# Experimental RF Workflow

This workflow shows how **theory, math, Python, and hardware** interact in my experimental base station. Focus is on exploration, measurement, and iteration rather than casual chatting.

## **1. Theory Layer (Maxwell & Circuit Concepts)**

- Fundamental electromagnetic principles:
  - Gauss’s Law → capacitor/voltage experiments
  - Faraday’s Law → coil/induction tests
  - Ampère’s Law → current/magnetic field exploration
  - Wave Equations → RF propagation & antenna behavior
- Predict outcomes before building circuits.

## **2. Math Layer**

- Calculate expected circuit behavior:
  - Resonant frequency: \( f = \frac{1}{2\pi\sqrt{LC}} \)
  - Impedance, voltage dividers, filter responses
  - Gain and SNR calculations
  - Fourier analysis for signals
- Compare predictions to measurements from hardware.

## **3. Python Layer**

- Data acquisition and analysis:
  - Read Arduino sensors via `pyserial`
  - Capture SDR signals for spectrum analysis
  - Plot waveforms, FFTs, and filter responses (`matplotlib`, `numpy`, `scipy`)
- Simulation and experiment planning:
  - Model filters, antennas, or propagation effects
  - Generate test waveforms for Arduino/DDS
- Automate experiments and log results for iteration.

## **4. Hardware Layer**

### **A. Control**
- **Arduino Uno/Nano**
  - Drives DDS modules (Si5351, AD9833)
  - Controls switches, sensors, and circuits
  - Handles timing-critical operations
- **Raspberry Pi**
  - SDR interface, signal analysis, and logging
  - Optional GUI for experiment control
  - Interfaces with Arduino for automated testing

### **B. Signal Generation**
- **Si5351 Module** → HF/VHF square waves
- **AD9833 Module** → precise sine/triangle signals
- Optional analog signal generator for lab measurements

### **C. RF Front-End**
- **AT‑878UVII Plus**
  - VHF/UHF transceiver for monitoring, low-power experiments, and digital mode testing
  - Receives Arduino/DDS signals for comparison
  - Optional PC control for logging, scanning, or experiment automation
- Experimental transceivers or QRP modules
- Filters, amplifiers, matching networks
- Antennas (dipoles, loops, verticals)
- Dummy loads for safe testing

### **D. Measurement**
- SDR (RTL-SDR, HackRF/LimeSDR)
- Oscilloscope / multimeter
- Frequency counter (optional)
- Compare signals received on AT‑878 with SDR readings

### **E. Optional Benchmark / Real-World Layer**
- **IC‑7300 HF Transceiver**
  - Observe real HF propagation
  - Compare DIY signals to a professional rig
  - Optional CAT/USB control for logging and experiment integration

---

## **5. Workflow: Experiment Cycle**

1. **Theory → Prediction**  
   - Use Maxwell’s equations and math to calculate expected behavior.
2. **Design → Build**  
   - Assemble circuits on breadboard; program DDS/Arduino to generate signals.
3. **Measure → Observe**  
   - Use SDR, AT‑878, or oscilloscope to capture signals.
4. **Analyze → Compare**  
   - Python processes measurements; compare to theoretical predictions.
5. **Iterate → Refine**  
   - Adjust components, waveforms, or antennas and repeat cycle.
6. **Optional Benchmark**  
   - IC‑7300 verifies real-world propagation and signal quality

---

### 💡 Notes

- **AT‑878 role:** VHF/UHF monitoring, low-power experiments, and digital mode testing. Complements Arduino/DDS + SDR.  
- **Arduino + DDS** = hardware signal generation & control  
- **Pi + SDR** = digital capture, analysis, visualization  
- **IC‑7300** = HF benchmark and safe real-world interface  
- **Workflow is modular**: start small (Arduino + DDS), expand with SDR + Pi, integrate AT‑878, and optionally IC‑7300 for HF verification.

