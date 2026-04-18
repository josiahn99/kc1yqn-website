---
layout: default
title: RF Roadmap
---

# RF Roadmap

## Purpose

My childhood curiosity about how the universe works returned strongly in 2025. Primarily, it was sparked by reading *Remembrance of Earth’s Past* by Liu Cixin and listening to the Daniel and Kelly's Extraordinary Universe podcast. I don't have a deep math or science background, and I'm not about to go make particle physics breakthroughs at CERN. However, amateur radio provides a unique, hands-on way to interact with experimental physics. 

The goal, ultimately, is to use RF experimentation and operation as a tool for understanding the underlying theory and math behind electromagnetics. 

## Initial Strategy

My launching point is using what I've learned about radio over the last few months with a HT and a tech license. So as to be able to operate and experiment on the HF airwaves this fall, my first step is to studying for the General exam, so that I can be on the HF airwaves in fall 2026. Along with the ARRL General Study Guide, I am complementing the knowledge needed for the General and Amateur Extra exams through the *Advanced Radio Theory Handbook* by Ron Bertrand, and [Electronics Tutorials](https://www.electronics-tutorials.ws/). 

After that, I will move towards a more general physics / electrical engineering study curriculum.

For now, I'm working on 


# Learning Philosophy

Concurrently with 
I'm currently structuring my learning around getting a strong handle on the General and Amateur Extra exam material. So as not to just memorize answers, I'm trying to apply the old addage of understanding something by being able to explain it. Thus for any concept covered on the exam, I'm considering the following two questions: 

- Would I be able to explain it to a 10 year old? 
- Project Hail Mary and Artemis II has seen a rise in the general public's interest in science-related ideas. Would I be able to demonstrate how the concept applies to those two things?

As I read over this roadmap, I fear I'm trying to hold myself to a graduate-level standard in a part-time hobby. I want to build on my high school calculus to eventually understand some deeper aspects like the wave equation or Maxwell's equations. But that's going to require some linear algebra, multivariable, and vector calculus—an ambitious goal for a part-time hobby. While it will be necessary to meet my goals, I am accepting this is a long-term plan. The focus should be depth over speed.  

I also don't want to get so bogged down in theory that I ignore actual operating or real-world experimentation, and so I've identified circuit and antenna experiments to ensure that I become proficient at operating and building. 

### Measurable outcomes (2026 - 2027)

- Pass the General and Amateur Extra exams, being able to provide a deeper understanding of each topic  
- Build and operate a basic HF station, and use it as a lab for observation, experimentation, and analysis  
- Complete and document at least 5 RF circuit / antenna experiments  

After this, the plan is a little more ambiguous. If I still want to get deeper into the theory and weeds after the Extra exam, I'll go further into undergraduate electromagnetics coursework (which sounds like a good idea on paper, but… yeah, let's see how it turns out).

---

## Antenna Experiments

Building on what I've learned about antenna theory and use so far of pre-made antennas (2m/70cm signal stick and slim jim), construct the following:

1. 20m / 40m dipole  
2. End-fed half-wave  
3. 2m Yagi  

For each of these, conduct experiments that test hypotheses regarding:

- Resonance, impedance, SWR  
- Signal reception and propagation quality  
- Effects of height, orientation, and the environment  

I will observe, measure, and analyze results using the following equipment:

- NanoVNA  
- RTL-SDR  
- Anytone-878  
- HF radio (to be purchased)  

In the spirit of the scientific method, I will control variables as much as possible, and where there is a mismatch between what I observe and what I expected, I will determine potential explanations. 

---

## Circuit Experiments

Breadboard, Manhattan-style, and PCB circuits are an opportunity to see basic electrical theory and RF in action.  with a focus on amplifier and oscillating circuits. I will also be reviewing QST Magazine and *On the Air* Magazine for ideas to improve my basic building abilities. 

Circuits I plan to build include:

- Class A amplifier  
- LC band-pass filter  
- Simple RF oscillator  
- Audio or RF amplifier  

I will also put these circuits together to build a signal chain of oscillator, filter, and amplifier to measure how each stage affects the signal and track distortion, bandwidth, and gain. 

Data to be recorded, where appropriate, includes:

- Frequency response  
- Signal amplitude  
- Filter bandwidth  

Equipment for this will include breadboards, basic electrical components, and a multimeter, signal generator, and oscilloscope for circuit testing.

### HF Station Experiments

I plan to establish a small HF station—likely an Icom IC-7300—that will function as the center of experimentation.

- Modular antenna switching  
- Measurement instrumentation for impedance, SWR, and signals  
- Digital logging of QSOs, propagation, and experiment notes  

This website will function as a lab notebook documenting hypotheses, experiments, measurements, and observations.

I have a strong interest in the ability of modern radios to interact so efficiently with computers. My setup will emphasize this relationship, with a Raspberry Pi (or similar) to be used for station control, SDR interfaces, and data collection. I will build upon my existing knowledge of Python and SQL to analyze measurements and visualize results, using libraries such as Pandas and Matplotlib.  

Another interest of mine is Geographic Information Systems, and I would ultimately like to combine that into the fold through QGIS and PyQGIS.

---

## Theory

I want to understand the theoretical framework behind the experiments and operating activities described above. As indicated above, I'm starting this off with *Advanced Radio Theory Handbook* by Ron Bertrand. After this, I'm planning on reviewing the ARRL Antenna Book. I also plan to brush off and extend my high school calculus, eventually diving into *Introduction to Electrodynamics*. With that in mind, the timeframe might look something like this:

### Now

- Ohm’s law → impedance  
- Complex impedance  
- Resonance  
- Transmission lines  
- Standing waves  
- Basic antennas  
- SNR / noise  
- Filters / bandwidth  
- Fourier analysis  

### Later

- Multivariable / vector calculus  
- Linear algebra  
- Maxwell’s equations  
- Wave propagation 
