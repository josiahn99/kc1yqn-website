---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

### Question
What kind of propagation can I expect for VHF/UHF under normal conditions and beyond?

### Goals  
- Understand local repeater infrastructure  
- Build a realistic baseline for VHF/UHF range  
- Create a framework for comparing antennas and tropospheric propagation  

### Background
Before I bought my first radio, I wondered whether I would hear much of anything on VHF/UHF. Living in suburban Massachusetts, there are quite a few repeaters regionally, but no wide coverage ones are particularly close to me. Quick research on the internet using the Line of Sight (LOS) formula indicated I would have about a 6-mile radius to work with. Not much, so my expections were low. 

Once I started operating though, I was pleasantly surprised! I was able to receive and work repeaters quite a bit further than I expected. Distances of 20, 30, or even 40 miles were apparently do-able. 

How was this possible, and why was my inital estimate so off? 

This page documents my process to learn the basic principles of VHF wave propogation. I start at a high-level, expanding my initial line of sight analysis, and over time hope to fill in the gaps with other factors. 

---

### Initial Prediction

A common starting point for VHF/UHF propagation is the radio horizon formula:


`d = 1.23 (√h₁ + √h₂)`


Where:  
- *d* = distance in miles  
- *h₁, h₂* = antenna heights in feet  

Initially, I simplified this too much and only considered my own antenna height:

`d ≈ 1.23 √h`

From a second-floor window (~23 ft), this gave:

`d ≈ 5.9 miles`

Not great. 

Now, granted I was not taking into consideration the height of the repeater, as I wanted this to be a conservative estimate. Not considering anything else, what would I be able to hear? 

However, if for example we assumed a repeater height of 100 feet and plug that into the equation: 

`d = 1.23 (√23 + √100)
d ≈ 18.2 miles`

Okay, so a tower height of 100 feet would make a significant difference in my reach. The fact that the height is squared means you only get twice the distance for 4 times the height, but even with that, 100 feet is sngificnat. Still, I wasn't sure of repeater heights in my area. Repeaterbook.com unfortunately does not include height data, so it's a matter of trying to piece what you can together from local ham clubs that have a page about their repeater. 

### Initial Observations
I bought my radio and excitedly programmed it with ~100 of the closest repeaters. In practice, I was able to hear signals from Boston, Providence, and Worcester—far beyond the ~6 miles predicted. There were stations 20, 30, or even 40 miles carrying nets that far exceeded what I had hoped!

Even using a modest upgraded handheld antenna (Signal Stick), this result didn’t make sense. Terrain, buildings, and trees should have reduced range further, not increased it.

This was great news, but clearly something was missing. 

### Refining the Model
As it turns out, that quick initial google search was leaving out some critical variables:

**1. Transmitter Height Matters**

The full equation includes both antennas:

`d = 1.23 (√h₁ + √h₂)`

Repeaters are often mounted on tall towers or elevated terrain, which dramatically increases range.

**2. Elevation Above Sea Level** 

A key realization was that antenna height is measured relative to mean sea level, not just height above ground.

My effective height became:

- Ground elevation: ~157 ft  
- Antenna height: ~23 ft  
- Total: ~180 ft  

This alone increased my radio horizon significantly.

### Spatial Analysis

To better understand coverage and take into account everything involved in the line-of-sight calculations, I built a simple model using:

- **USGS elevation data** for terrain  
- **Repeater data** from RepeaterBook.com (latitude/longitude)  
- **QGIS** for spatial analysis  

Since repeater antenna heights are not consistently available, I estimated a tower height (~100 ft) and combined it with ground elevation.

For each repeater, I calculated whether it should be within range using:

`d = 1.23 (√h₁ + √h₂)`

Where:  
- *h₁* = my elevation + antenna height  
- *h₂* = repeater elevation + estimated tower height  

I then compared this predicted range against actual distance.

This produced a simple classification of whether the station should be reachable or out of range.

**Examples**

1. W1BIM (Paxton, MA)

- Distance: ~40 miles  
- Elevation: ~1370 ft + ~100 ft tower  

`d ≈ 1.23 (√1470 + √180) ≈ 63.6 miles`

This explains why the repeater is consistently receivable.


2. W1BRI (Hopkinton, MA)

- Elevation: ~460 ft + ~100 ft tower  

`d ≈ 1.23 (√560 + √180) ≈ 45 miles`

Again, well within range.

---

### Results

The map below compares line-of-sight predictions to actual observations.

**TODO:** Insert map image

**TODO:** ~X% of repeaters predicted to be within range were actually observed.

---

### Limitations

This model is intentionally simplified and has several limitations:

- Repeater antenna heights are estimated  
- Terrain resolution is limited by dataset granularity  
- Buildings and vegetation are not included  
- Differences between 2m and 70cm are ignored  

Even after correcting for elevation, observed reception still exceeds line-of-sight predictions. The line-of-sight equation should be treated as a baseline, not a hard limit.

Additional propagation effects include:

- Atmospheric refraction extending the radio horizon  
- Diffraction allowing signals to bend over terrain  
- Partial Fresnel zone clearance enabling usable signals  
- Repeater placement and power improving coverage  

---

### Next Steps

With repeaters and terrain now in QGIS, the next step is refining the model:

- Incorporate **Fresnel zone analysis**
- Use **Longley-Rice (ITM)** via tools like [pycraf](https://github.com/bwinkel/pycraf)  
- Compare predicted vs observed reception  
- Analyze **tropospheric ducting** events  

While repeater height data is limited, rough estimates combined with terrain data should allow for increasingly accurate modeling.
