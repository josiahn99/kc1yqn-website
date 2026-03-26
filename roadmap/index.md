---
layout: default
title: Learning Plan
---

# RF Roadmap

## Purpose

My childhood curiosity about how the universe works returned strongly in 2025. Primarily, it was sparked by reading Remembrance of Earth’s Past by Liu Cixin and listening to the Daniel and Kelly's Extraordinary Universe podcast. Both include the theme of theoritcal and applied physics being critical to civilizational progress and understanding of reality. Now, as someone who has chosen a social science route since college, I'm not about to go make particle physics breakthroughs at CERN. Amateur radio provides a unique way to learn more about physics in a hands-on way.

The goal is to better understand physics by building a solid foundation in RF communication and theory.

## Initial Strategy

I'm structuring my learning in 2026 around getting a strong handle on the General and Amateur Extra exam material. My goal is to be able to provide an explanation, at least on a high level, for any of the questions on the pool.  while also starting small experiments.

I struggle with the learning curve around this and how aggressively to tackle different topics. I want to build on my high school calculus to eventually understand some deeper aspects like the Wave Equation or Maxwell's equations. But that's going to require some linear algebra, multivariable, and vector calculus - an ambitious goal for a part-time hobby, so I'm trying not to commit hard to that yet. 

I also don't want to get so bogged down on theory that I ignore actual operating or real-world experimenting, and so I've identified cicruit and antenna experiments to ensure that I become proficient at operating and building. 

### Measurable outcomes (2026)

* Pass the General and Amateur Extra exams, having a high-level explanation for any question
* Build and operate a basic HF station, and use it as a lab for observation, experimentation, and analysis
* Complete and document at least 5 RF circuit / antenna experiments

After this, the plan will evolve. If I still want to get deeper into the theory and weeds after the Extra exam, I'll go further into undergraduate electromagnetics coursework. It sounds like a good idea on paper, but... yeah, let's see how it turns out. 

---

## Antenna Experiments

Building on what I've learned about antenna theory and use so far of pre-made antennas (2m/70cm signal stick and slim jim), construct the following:

1. 20m / 40m dipole  
2. End-fed half-wave
3. 2m Yagi

For each of these antennas, measure, record, and compare:
Resonance, impedance, SWR
Signal reception and propogation quality 
Effects of height and orientation

A combination of my RTL-SDR, Anytone-878, and a HF radio to be purchased will be utilized with these antennas. 

---

## Circuit Experiments

Breadboard and PCB circuits are an opportunity to see basic electrical theory and RF in action. For now, I'm working on complementing the knowledge needed for the General and Amateur Extra exams through Advanced Radio Theory Handbook by Ron Bertrand, and [Electronics Tutorials](https://www.electronics-tutorials.ws/), with a focus on amplifier and oscillating circuits. 

Circuits I plan to build include: 

   - Class A amplifier
   - LC band-pass filter  
   - Simple RF oscillator
   - Audio or RF amplifier

Data to be recorded, where appropriate, includes: 
  - Frequency response  
  - Signal amplitude  
  - Filter bandwidth  

I will also be reviewing QST Magazine and On the Air Magazine for ideas to improve my basic building abilities. 

### HF Station Experiments

I plan to establish a small HF station - likely an Icom IC-7300 - that will function as the center of experimentation.

* Modular antenna switching  
* Measurement instrumentation for impedance, SWR, and signals  
* Digital logging of QSOs, propagation, and experiment notes

This website will function as a lab notebook documenting experiments, measurements, and observations.

I have a strong interest in the ability of modern radios to interact so efficiently with computers. My set up will emphasize this relationshipo, with Raspberry Pi (or similar) to be used for station control, SDR interfaces, data collection. I will build upon my existing knowledge of Python and SQL to analyze measurements and visualize results, using libraries such as Pandas and Matplotlib.  

Another interest of mine is Geographic Information Systems, and would ultimately like to combine that into the fold through QGIS and PyQGIS.

## Theory

I want to understand the theoretical framework behind the experiments and operating activities described above. As indicated above, I'm starting this off with Advanced Radio Theory Handbook by Ron Bertrand. After this, I'm planning on reviewing the ARRL Antenna Book. If I ultimately do decide to puruse a more math intensive, deeper understanding approach, I would then focus on brushing off and extending my high school calculus, eventually diving into Introduction to Electrodynamics. WIth that in mind, the timeframe might look something like this:

### Year 1
   - Ohm’s law
   - Impedance
   - Resonance
   - Standing waves
   - Transmission lines
   - Basic antenna behavior

### Year 2–3
   - Complex impedance
   - Fourier decomposition
   - Filters and bandwidth
   - Noise and signal-to-noise ratio

### Later
   - Vector calculus
   - Maxwell’s equations
   - Wave propagation

---

## Equipment

Measurement tools: 

* Breadboard & components  
* Signal generator / oscillator for circuit testing
* Raspberry Pis (3/4)  
* RTL-SDR receiver  
* AnyTone AT-D878UVII Plus
* HF radio and accessories (likely the Icom IC-7300)  
