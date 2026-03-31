---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

## Summary

**Question:** What kind of propagation can I expect for VHF/UHF under normal conditions and beyond?

**Goals:**  
- Understand local repeater infrastructure  
- Build a realistic baseline for VHF/UHF range  
- Create a framework for comparing antennas and tropospheric propagation  

Before I bought my first radio, I expected I wouldn’t hear much of anything. Initial research seemed to confirm that assumption. In practice, I found the opposite—I was able to receive and work repeaters far beyond what I thought was possible.

This write-up documents how that gap between expectation and reality led me to refine my understanding of propagation.

---

## Initial Expectation: Line-of-Sight

A common starting point for VHF/UHF propagation is the radio horizon formula:


d = 1.23 (√h₁ + √h₂)


Where:  
- *d* = distance in miles  
- *h₁, h₂* = antenna heights in feet  

Initially, I simplified this too much and only considered my own antenna height:


d ≈ 1.23 √h


From a second-floor window (~23 ft), this gave:


d ≈ 5.9 miles


That suggested very limited range—likely not enough to reach wide-area repeaters.

---

## Reality: Much Greater Range

In practice, I was able to receive signals from Boston, Providence, and Worcester—far beyond the ~6 miles predicted.

Even using a modest upgraded handheld antenna (Signal Stick), this result didn’t make sense if the model were complete. Terrain, buildings, and trees should have reduced range further, not increased it.

Clearly, something was missing.

---

## Refining the Model

### 1. Transmitter Height Matters

The full equation includes both antennas:


d = 1.23 (√h₁ + √h₂)


Repeaters are often mounted on tall towers or elevated terrain. That dramatically increases range.

### 2. Elevation Above Sea Level

A key realization was that antenna height is measured relative to mean sea level, not just height above ground.

My effective height became:

- Ground elevation: ~157 ft  
- Antenna height: ~23 ft  
- Total: ~180 ft  

This alone increased my radio horizon significantly.

---

## Why Reality Still Exceeds the Model

Even after correcting for elevation, observed reception still exceeded predictions. This indicates additional propagation effects:

- **Atmospheric refraction** extends the radio horizon beyond geometric line-of-sight  
- **Diffraction** allows signals to bend over terrain  
- **Fresnel zone clearance** enables signals even without perfect visibility  
- **High repeater placement and power** improve coverage  
- **Receiver sensitivity** allows detection of weak signals  

The line-of-sight equation should be treated as a **baseline**, not a hard limit.

---

## Data-Driven Approach

To better understand coverage, I built a simple model using:

- **USGS elevation data** for terrain  
- Repeater data from RepeaterBook (latitude/longitude)  
- **QGIS** for spatial analysis  

Since repeater antenna heights are not consistently available, I estimated tower height (~100 ft) and combined it with ground elevation.

---

## Method

For each repeater, I calculated whether it should be within line-of-sight range using:


d = 1.23 (√h₁ + √h₂)


Where:  
- *h₁* = my elevation + antenna height  
- *h₂* = repeater elevation + estimated tower height  

I then compared this predicted range against actual distance.

This produced a simple classification:
- **1** = predicted reachable  
- **0** = predicted out of range  

---

## Examples

### W1BIM (Paxton, MA)

- Distance: ~40 miles  
- Elevation: ~1370 ft + ~100 ft tower  


d ≈ 1.23 (√1470 + √180) ≈ 63.6 miles


This comfortably explains why the repeater is consistently receivable.

---

### W1BRI (Hopkinton, MA)

- Elevation: ~460 ft + ~100 ft tower  


d ≈ 1.23 (√560 + √180) ≈ 45 miles


Again, well within range.

---

## Key Insight

The most important realization was that my “23 ft antenna height” was misleading. My true effective height was closer to ~180 ft when accounting for elevation.

That alone expanded my expected range from ~6 miles to over 15 miles—and much further when combined with repeater height.

---

## Limitations

This model is intentionally simplified and has several limitations:

- Repeater antenna heights are estimated  
- Terrain resolution is limited by dataset granularity  
- Buildings and vegetation are not included  
- Differences between 2m and 70cm are ignored 
