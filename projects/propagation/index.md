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


`d = 1.23 (√h₁ + √h₂)`


Where:  
- *d* = distance in miles  
- *h₁, h₂* = antenna heights in feet  

Initially, I simplified this too much and only considered my own antenna height:


`d ≈ 1.23 √h`


From a second-floor window (~23 ft), this gave:


`d ≈ 5.9 miles`


That suggested very limited range—likely not enough to reach wide-area repeaters.

---

## Reality: Much Greater Range

I created a codeplug with ~100 of the closest repeaters to see how far I could receive. In practice, I was able to hear signals from Boston, Providence, and Worcester—far beyond the ~6 miles predicted.

Even using a modest upgraded handheld antenna (Signal Stick), this result didn’t make sense. Terrain, buildings, and trees should have reduced range further, not increased it.

Clearly, something was missing.

---

## Refining the Model

### 1. Transmitter Height Matters

The full equation includes both antennas:


d = 1.23 (√h₁ + √h₂)


Repeaters are often mounted on tall towers or elevated terrain, which dramatically increases range.

### 2. Elevation Above Sea Level

A key realization was that antenna height is measured relative to mean sea level, not just height above ground.

My effective height became:

- Ground elevation: ~157 ft  
- Antenna height: ~23 ft  
- Total: ~180 ft  

This alone increased my radio horizon significantly.

---

## Why Reality Still Exceeds the Model

Even after correcting for elevation, observed reception still exceeds line-of-sight predictions. This indicates additional propagation effects:

- Atmospheric refraction extends the radio horizon  
- Diffraction allows signals to bend over terrain  
- Partial Fresnel zone clearance can still support usable signals  
- Repeater placement and power improve coverage  

The line-of-sight equation should be treated as a baseline, not a hard limit.

---

## Data-Driven Approach

To better understand coverage, I built a simple model using:

- **USGS elevation data** for terrain  
- **Repeater data** from RepeaterBook (latitude/longitude)  
- **QGIS** for spatial analysis  

Since repeater antenna heights are not consistently available, I estimated a tower height (~100 ft) and combined it with ground elevation.

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


This explains why the repeater is consistently receivable.

---

### W1BRI (Hopkinton, MA)

- Elevation: ~460 ft + ~100 ft tower  


d ≈ 1.23 (√560 + √180) ≈ 45 miles


Again, well within range.

---

## Limitations

This model is intentionally simplified and has several limitations:

- Repeater antenna heights are estimated  
- Terrain resolution is limited by dataset granularity  
- Buildings and vegetation are not included  
- Differences between 2m and 70cm are ignored  

---

## Next Steps

With repeaters and terrain now in QGIS, the next step is refining the model:

- Incorporate **Fresnel zone analysis**
- Use **Longley-Rice (ITM)** via tools like [pycraf](https://github.com/bwinkel/pycraf)  
- Compare predicted vs observed reception  
- Analyze **tropospheric ducting** events  

While repeater height data is limited, rough estimates combined with terrain data should allow for increasingly accurate modeling.

---

## Lessons Learned

This process reinforced the value of understanding how equations are derived rather than simply applying them. Expanding the model to include both antenna heights and elevation dramatically changed the expected results.

More importantly, it showed that formulas are only a starting point. Real-world propagation is shaped by multiple interacting effects, and observation is essential to refining theory.

Amateur radio offers the ability to explore this at any level—from basic operation to detailed modeling—and the depth is always there for those who want to go further.
