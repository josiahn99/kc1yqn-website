---
layout: default
title: Learning Plan
---

# RF Roadmap

## Motivation

My childhood curiosity about how the universe works has returned strongly, sparked by reading Remembrance of Earth’s Past by Liu Cixin and listening to the Daniel and Kelly's Extraordinary Universe podcast.

Amateur radio provides a unique way to interact directly with electromagnetic phenomena rather than only reading about them.

The goal is to build a solid foundation in RF and approach amateur radio like a laboratory — measuring, tweaking, and learning from each experiment.

This roadmap is organized around three interrelated areas:

* Operating & Experimenting  
* Theory  
* Related Technical Interests  

Each section supports the others and makes progress measurable.

---

## Initial Objective

The first milestone is to get a strong handle on the General and Amateur Extra exam material while also starting small experiments.

Measurable outcomes (6 months):

* Pass the General and Amateur Extra exams  
* Build and operate a basic HF station  
* Complete and document at least 5 RF experiments with notes, graphs, or photos  

After this, the plan will evolve toward more advanced experiments and deeper math, including concepts from Maxwell’s electromagnetic theory.

---

## Operating & Experimentation

This is where the “hands-on lab” happens. Every transmission, antenna test, or codeplug tweak is a small experiment if treated that way.

### Antenna Experiments

Focus on antennas that can be adjusted and measured easily. Within the first year:

1. 20 m dipole  
   - Measure resonance and impedance with NanoVNA-H4  
   - Adjust length and log resonance shifts  
   - Record SWR bandwidth at different heights  

2. End-fed half-wave  
   - Compare feedpoint impedance and bandwidth with dipole  
   - Observe differences in received signal quality
     
3. 2m Yagi
   - Measure directional gain and front-to-back ratio
   - Test reception and transmission on local VHF repeaters
   - Log differences between horizontal and vertical polarization
   - Evaluate effects of mounting height and orientation
    
4. Height and location tests  
   - Compare performance at 10 ft, 20 ft, 30 ft  
   - Try near windows, indoors vs. outdoors, different floors  

5. Performance tracking  
   - Collect signal reports using FT8 and PSK Reporter  
   - Analyze how antenna type, height, and orientation influence reception  

Deliverables: log at least 5 antenna experiments with graphs or notes comparing results.

---

### Circuit Experiments

Breadboard circuits are an opportunity to see basic electrical theory and RF in action. Within 12 months:

* Build three circuits such as:  
  - LC band-pass filter  
  - Simple RF oscillator  
  - Audio or RF amplifier  

* Measure and record:  
  - Frequency response  
  - Signal amplitude  
  - Filter bandwidth  

Reference: [Electronics Tutorials](https://www.electronics-tutorials.ws/)  

Every circuit should include a mini lab report: what was built, how I measured it, and what I observed.

---

### Propagation & Operating Experiments

Operating isn’t just talking — it’s collecting RF data:

* Log at least 100 contacts, but treat them as data points: signal strength, time, mode, and band.  
* Run three structured propagation tests using FT8 to track path conditions.  
* Record SNR, signal clarity, and how antennas and location affect results.  

The goal is to learn patterns, not just accumulate contacts.

---

### Experimental Station Development

The goal here is to set up a small HF station - likely an Icom IC-7300 - that will function as the center of experimentation. Within 12 months:

* Modular antenna switching  
* Measurement instrumentation for impedance, SWR, and signals  
* Digital logging of QSOs, propagation, and experiment notes  

---

## Theory

I want to understand the theoretical framework behind the experiments and operating activities described above.

Resources:

* Advanced Radio Theory Handbook by Ron Bertrand  
* Later: ARRL Antenna Book  
* Eventually: Introduction to Electrodynamics  

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

## Instrumentation & Analysis

This website will function as a lab notebook documenting experiments, measurements, and observations.

Raspberry Pi systems will be used for station control, SDR interfaces, and data collection. Python will be used to analyze measurements and visualize results using libraries such as Pandas and Matplotlib. 

Goal: publish at least 5 experiments or notes within the first year, each with observations, graphs, and conclusions.

---

## Equipment

Measurement tools: 

* Breadboard & components  
* Signal generator / oscillator for circuit testing
* Raspberry Pi  
* USB SDR receiver for spectral observation  
* AnyTone AT-D878UVII Plus
* Python analysis of signal reports

Planned Purchases:

* HF radio and accessories (likely the Icom IC-7300)  


