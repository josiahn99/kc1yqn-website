---
layout: default
title: Learning Plan
---
# Learning Plan

# Returning to Science

I stepped away from math and science as a kid—because, spoiler, it was hard. Now I’m back, driven by curiosity and the satisfaction of figuring things out. Amateur radio caught my attention after reading *Remembrance of Earth’s Past* by Liu Cixin and listening to [Daniel and Kelly’s Extraordinary Universe podcast](https://podcasts.apple.com/us/podcast/daniel-and-kellys-extraordinary-universe/id1436616330). Both reignited my fascination with how the universe works, and ham radio provides a way to explore that curiosity hands-on through the electromagnetic spectrum.

---

# Operating and Experimenting

My time is often limited—commutes or late nights—but even small experiments are valuable. I’m starting as a Technician and working toward General and Amateur Extra. My approach emphasizes **understanding, not just passing exams**.

Key areas of focus:

- **Antennas:** experimenting with designs like 2 m Yagi and 40 m dipole  
- **Circuits:** building and testing Arduino/DDS setups, filters, and small RF front ends  
- **Logging and operating:** recording QSOs on BrandMeister and eventually HF  
- **Station building:** creating a modular, experimental setup rather than a conventional “shack”  

Even in hands-on activities, I aim to connect with the underlying **math and physics**: resonance in LC circuits, impedance, signal propagation, and wave behavior.

---

# Theory and Math

To build a solid foundation, I’m working through Bertrand’s *Advanced Radio Theory Handbook*. The goal is to reconnect with the relevant mathematics—calculus, complex numbers, and Maxwell’s equations—so that the experiments and observations make sense.

Key theoretical topics:

- Resonance and impedance in circuits and antennas  
- Wave propagation and polarization  
- Fourier analysis and signal decomposition  
- Maxwell’s equations as a framework for understanding electromagnetic behavior  

Even simple experiments become more meaningful when the results can be linked back to these principles.

---

# Connected Interests

Amateur radio naturally connects to other technical hobbies:

- **Website as lab notebook:** documenting experiments, designs, and observations  
- **Raspberry Pi projects:** using Pi as a controller, SDR interface, or data logging platform  
- **Python experimentation:** analyzing data, generating plots, or controlling experiments  

This site serves both as a record and as a way to link practical experiments with the theory behind them.

---

# Experimental RF Workflow

The setup combines hardware, observation, and theory to create a learning loop that emphasizes experimentation.

## **1. Signal Generation (Arduino + DDS)**

- Generate signals with Si5351 or AD9833 modules  
- Explore circuit behavior: filters, LC tanks, and simple modulations  
- Apply theory: resonance, impedance, and waveform shaping

## **2. Observation and Measurement (SDR + Scope)**

- Capture and visualize signals using SDRs (RTL-SDR, HackRF, or LimeSDR)  
- Use oscilloscopes or multimeters to measure voltage, current, and waveform  
- Compare observed behavior with theoretical predictions

## **3. Transceivers in Practice**

- **AT‑878UVII Plus:**  
  - Monitor and receive VHF/UHF signals  
  - Experiment with low-power transmissions and digital modes  
- **IC‑7300 (HF rig, later stage):**  
  - Observe real-world HF propagation  
  - Validate experimental setups and compare lab vs. real-world signals

## **4. Learning and Iteration**

1. Build a circuit or generate a test signal  
2. Observe the results with SDR, AT‑878, or scope  
3. Analyze and visualize with Python  
4. Adjust components, waveforms, or antennas  
5. Repeat the cycle and gradually scale to HF experiments

---

### Key Notes

- **Arduino + DDS:** signal generation and hands-on experimentation  
- **Pi + SDR:** observation, logging, and analysis  
- **AT‑878:** VHF/UHF experimentation, monitoring, and digital modes  
- **IC‑7300:** HF verification and real-world propagation testing  
- **Underlying theory and math:** resonance, impedance, wave propagation, and Maxwell’s equations inform every experiment  
- Modular, expandable setup allows gradual progression from simple experiments to more advanced RF exploration
