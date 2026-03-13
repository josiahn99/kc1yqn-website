---
layout: default
title: Learning Plan
---

RF Learning Plan

### Motivation

My childhood curiosity about how the universe works has come back strong, sparked by reading *Remembrance of Earth’s Past* by Liu Cixin and listening to the *Daniel and Kelly's Extraordinary Universe* podcast. Amateur radio is the perfect playground to explore the electromagnetic spectrum while logging observations and testing ideas.  

The goal is to build a solid foundation in RF and approach it like a lab — measuring, tweaking, and learning from each experiment.

This roadmap is organized around three interrelated areas:

* Operating & Experimentation  
* Theory  
* Connected Technical Interests  

Each section supports the others and helps make progress measurable.

---

### Initial Objective

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
     
3. 2 m Yagi
  - Measure directional gain and front-to-back ratio
  - Test reception and transmission on local VHF repeaters
  - Log differences between horizontal and vertical polarization
  - Evaluate effects of mounting height and orientation
    
3. Height and location tests  
   - Compare performance at 10 ft, 20 ft, 30 ft  
   - Try near windows, indoors vs. outdoors, different floors  

4. Performance tracking  
   - Collect signal reports using FT8 and PSK Reporter  
   - Analyze how antenna type, height, and orientation influence reception  

Deliverables: log at least 3 antenna experiments with graphs or notes comparing results.

---

### Circuit Experiments

Breadboard circuits are an opportunity to see RF in action. Within 12 months:

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

The station is your lab bench. Within 12 months:

* Modular antenna switching  
* Measurement instrumentation for impedance, SWR, and signals  
* Digital logging of QSOs, propagation, and experiment notes  

Start with a small HF setup — likely an Icom IC-7300 — and expand from there. Every setup change is an experiment.

---

## Theory

Theory is what lets you understand why experiments behave as they do. Resources:

* Advanced Radio Theory Handbook by Ron Bertrand  
* Later: ARRL Antenna Book  
* Eventually: Introduction to Electrodynamics  

First-year goals:

* Understand Ohm’s law, impedance, resonance, SWR, transmission line basics  
* See how simple circuits produce standing waves and resonance  
* Start experimenting with Fourier decomposition of signals  

Long-term (2–5 years):

* Review calculus, complex numbers, and linear algebra  
* Apply Fourier analysis to signals  
* Study vector calculus and Maxwell's equations  
* Connect math concepts to actual lab measurements  

---

## Connected Technical Interests

This website will serve as a lab notebook, documenting experiments, results, and designs.
Raspberry Pis will be used for controllers, SDR interface, and logging / analyzing data.  
Python will analyze measurements, visualize propagation and circuit results with Pandas and Matplotlib  

Goal: publish at least 5 experiments or notes within the first year, each with observations, graphs, and conclusions.

---

## Equipment

Currently Available:

* Breadboard & components  
* Signal generator / oscillator  
* Raspberry Pi  
* USB SDR receiver  
* AnyTone AT-D878UVII Plus  

Planned Purchases:

* NanoVNA-H4  
* HF radio and accessories (likely Icom IC-7300)  
