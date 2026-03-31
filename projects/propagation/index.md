---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

### Summary
**Question:** What kind of propogation can I expect, under normal conditions and beyond, for VHF / UHF?  

**Goals:** Understand local repeater infrastructure and how VHF / UHF radio waves propogate. 
Develop a baseline for comparing future antennas and troposcopic ducting.

Before I bought my first radio, I was concerned I wouldn't hear anything. Initial Google searches seeemed to confirm this. I realized as soon as I started listening that I significantly underestimated my reception and have been able to work wide coverage repeaters much further than expected. 

Below is a summary of my initial thinking, how I've revised my thinking based on observations.  

### Initial Expectation - Line of Site Calculations

The primary determinant for line-of-site VHF/UHF communication is the earth's curvature. Derived from the pythagorean theorem, the equation for distance is based on the heights of the transmitting station (as I learned, there's more to it):

d = 1.23 * sqrt(h)

Where d is in miles, h is in feet.

From a second floor window, I have about 23 feet of height, and plugging that in, I got a circle with radius 5.9 miles. Not bad, but also not great. Not enough to reach any wide area repeaters. I was certainly concerned I wouldn't be able to transmit or receive much of anything. 

### Reality 

I did read early on how the rubber duck antenna that comes with the radio is very meager, so though I wasn't ready to go with a permanent or semi-permanent antenna, I upgraded to a [signal stick] (https://signalstuff.com). However, even with this, I shouldn't be able to magically see over the edge of the earth. 

I created a codeplug that had 100 or so of the closest repeaters to me, just to see exactly how far I could receive. Surprisingly, doing a scan through this list of stations I was able to hear quite a bit! Signals from Boston, Providence, and Worcester! Much beyond the 6 miles I had expected. While mostly ?I just heard wide coverage repeaters, I heard a few more local nets and Skywarn nets during a large snowstorm it wasn't just a fluke that I was able to hear quite a bit further in every direction. 

Why such better results than expected? If anything, wouldn't trees, houses, and hills get in the way and make my line-of-sight even worse?

Diving a bit deeper into the line-of-sight formula and how it's derived (such as [continuouswave.com](https://continuouswave.com/radio/radioHorizon.html)), it turned out I was missing a key item: 

d = 1.23( sqrt(h1) + sqrt(h2))

Where d is in miles, h1 is the receiver height in feet h2 is the transmitter height in feet. 

Obviously, if the transmitter happens to be on top of a mountain, it's going to reach a lot further, or if my station is higher up than somewhere closer to the coast, that's going to help too. Not only that, h1 and h2 are based on mean elevation above sea level. This bumps my 23 feet to ___ or so.

### Further Data Collection
A more complete answer for why my signal was carrying much further than expected was going to need to be able to fill in all the variables of the line-of-sight equation. Specifically, I needed two datasets:

**Ground elevation data** can be accessed through the United States Geological Survey.

**Repeater locations** can be downloaded from [repeaterbook.com](www.repeaterbook.com) as a .csv file with lat/long data. Unfortunately, actual antenna heights are not well tracked, so this provides nothing about the elevation. To supplement this data gap, I used USGS elevation data and added a modest __ feet to account for an average tower height. 

For this, I used the free, open-source [QGIS] (https://qgis.org/).

### Results

I used these datasets to calculate a column in QGIS that will be 1 if the repeater should be within range, or 0 if too far away. The formula being: 

if(1.23*("elevation1"*3.28) ^ 0.5 + 13.41 > distance, 1, 0)

The map below shows a summary of my results, with distances and heights for key repeaters I've reached. 

A couple examples: 

The W1BIM repeater in Paxton, MA is about 40 miles away, perched on top of ___ . Using the line of site equation for this one, estimating a ground elevation of 1370 feet, plus a repeater height of 100 feet, we get:

d = 1.23(sqrt(1370+100) + sqrt(157+23)) 
= 63.6 miles

Well within range! 

The [W1BRI repeater](https://mmra.org) in Hopkinton, MA is at about a 460 foot elevation, with a 100 foot tower, so the calculation is:

d = 1.23(sqrt(460+100) + sqrt(157+23))
= 45 miles

The key thing here is that even removing the aided ability from a repeater much higher up, my base elevation was not 23 feet - it was ground elevation of 157 + 23 feet. Making my line of sight radius: 16.5 miles! This seems like an obvious point now that I've thought it through, but simply didn't occur to me before looking at the ground elevation data. shows the value of thinking things through.  

### Limitations 
At this point, I am forming a baseline with stations I can receive, as this is easier to accomplish. 

For transmission, there is the obvious question of whether a "monitoring" call out to a repeater is being heard clearly or if no one is listening or wanting to answer. Nets where viable are the way around this.

### Next Steps

Now that I have inputted repeaters and topographical data into QGIS, there is an opportunity for a lot more analysis to align observations with theory. The envelope on how far I can receive is much greater than initially expected, but there is still room to investigate exactly exactly how far I can reach. There isn't generally accurate data on repeater heights, but I can do rough estimates, and use topographical data to fill in the blanks. Eventually, I'd also like to incorporate freznel zones into the analysis and use a Python package such as [pycraf] (https://github.com/bwinkel/pycraf), to incorporate the Longley-Rice / ITM propagation model. 

I would also like to be able to use this baseline analysis to compare results from topospheric propogation. This [post on Reddit] (https://www.reddit.com/r/amateurradio/comments/oumzn4/reverse_engineering_hepburn_propagation_forecast/) from a few years ago speaks to two existing resources for studying tropo propogation that will be useful as well.  

## Lessons Learned

The key is that being above the earth at all, even if only a few hundred feet, makes a very large difference. This speaks to the value of understanding how equations are derived rather than just plugging in numbers to a formula. In this case, expanding the triangle is a huge factor.

The moral of the story here is, whenever possible, go beyond blindly following equations and think about what they mean. 

However, it's also a perfect example of how many levels there are to amateur radio and why I'm so glad I fell into this hobby. 

None of these is better than any other. It's like a giant puzzle with a bunch of smaller puzzles, you can stop at any time you feel comfortable and feel good about what you're doing. But the option is always there to go deeper. 
