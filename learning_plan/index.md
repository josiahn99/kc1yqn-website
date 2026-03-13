---
layout: default
title: Learning Plan
---

# RF Learning Plan

### Motivation

Recently, my childhood fascination with understanding how the universe works has been reignited. This was largely sparked by reading *Remembrance of Earth’s Past* by Liu Cixin and listening to the *Daniel and Kelly's Extraordinary Universe* podcast. Amateur radio provides a practical way to explore the electromagnetic spectrum and communicate scientific ideas.

My goal is to build a solid foundation in RF that allows me to explore radio scientifically rather than casually. To support this, I have developed a learning roadmap organized around three complementary areas:

* Operating
* Experimentation
* Theory

Each area reinforces the others and provides a balanced path toward deeper understanding.

---

### Initial Objective

The initial objective is to develop a strong understanding of the material covered on the General and Amateur Extra exams.

Measurable outcomes

Within 6 months:

* Pass the General and Amateur Extra exams
* Build and operate an HF station
* Complete and document at least 5 RF experiments

After this milestone, the learning path will be reassessed with the goal of expanding into amateur science projects and deeper mathematical foundations of RF, including concepts derived from James Clerk Maxwell’s electromagnetic theory.

---
## Operating and Experimentation

Operating will primarily be used as a data collection and experimentation platform rather than solely for casual communication. On-air activity will support antenna testing, propagation observation, and RF measurement.

### Antenna Experiments

Initial experiments will focus on simple wire antennas that allow controlled adjustments and repeatable measurements.

Within the first year:

1. Build a 20 m dipole antenna

   - Measure resonance and impedance using a NanoVNA-H4  
   - Adjust antenna length and record resonance shifts  
   - Record SWR bandwidth

2. Build an end-fed half-wave antenna

   - Compare feedpoint impedance and bandwidth with the dipole  
   - Evaluate matching network behavior

3. Test antenna height effects

   - Record SWR and impedance at different heights (10 ft, 20 ft, 30 ft)  
   - Compare received signal reports

4. Compare antenna performance using digital propagation data

   - Use FT8 to collect signal reports  
   - Analyze results using PSK Reporter data

Deliverables

- At least 3 documented antenna experiments
- Published measurement graphs and notes on the website
- Comparison of predicted vs measured antenna behavior

---

### RF Circuit Experiments

Basic RF electronics experiments will be performed using breadboards and simple circuits.

Topics include:

- oscillators
- filters
- amplifiers
- mixers

Measurable outcomes (within 12 months)

Build three working RF circuits, such as:

- LC band-pass filter
- simple RF oscillator
- audio or RF amplifier

Measure and record:

- frequency response
- signal amplitude
- filter bandwidth

Reference materials will include tutorials from  
[Electronics Tutorials](https://www.electronics-tutorials.ws/).

---

### Propagation and Signal Experiments

On-air activity will be used to collect measurable RF data.

Experiments may include:

- propagation observations using FT8
- antenna performance comparisons
- signal strength and SNR measurements
- time-of-day and band condition observations

Goals (first year)

- Collect signal reports from at least 100 stations
- Conduct three structured propagation experiments
- Record and analyze signal reports using Python

---

### Experimental Station Development

The station will be designed to support experimentation and measurement.

Design priorities:

- modular antenna switching
- measurement instrumentation
- digital logging and data collection

Milestone

Within 12 months:

Build a small HF experimental station centered around an HF transceiver such as the Icom IC-7300.

---

# Theory

Theory will be studied alongside experimentation so that concepts can be tested in practice.

Initial resources:

* Advanced Radio Theory Handbook by Ron Bertrand

Future resources:
* ARRL Antenna Book
* Introduction to Electrodynamics

Learning milestones

Within 12 months:

Gain practical understanding of:

* Ohm’s law and impedance
* resonance in LC circuits
* standing waves and SWR
* basic transmission line theory
* Fourier decomposition of signals

Long-term goals (2-5 years):

Develop working familiarity with the mathematical tools underlying RF engineering:

* Calculus review
* Complex numbers
* Linear algebra
* Fourier analysis
* Vector calculus
* Maxwell's equations

---

# Connected Technical Interests

This website will serve as an experimental notebook, a place to publish results, and a technical learning sandbox.

Raspberry Pi systems will be used for data logging, SDR experimentation, and RF measurement automation

Python will be used to analyze RF measurements, visualize experiment results, and process propagation data. Target tools include Pandas and Matplotlib.

Publish at least 5 documented experiments or technical notes within the first year.

---

# Equipment

### Currently Available

* Breadboard and electronic components
* Signal generator / oscillator
* Raspberry Pi
* USB SDR receiver
* AnyTone AT-D878UVII Plus

### Planned Purchases

* NanoVNA-H4
* HF radio and accessories
  (currently considering the Icom IC-7300)

---

# Evaluation

Progress will be reviewed every 6 months.

Key indicators of progress:

* number of experiments completed
* data collected and analyzed
* concepts understood well enough to explain clearly
* documentation published on the website

The goal is not simply to accumulate equipment or contacts, but to gradually develop the ability to observe, measure, and reason about RF systems scientifically.
