---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

### Summary
**Question:** What kind of propogation can I expect, under normal conditions and beyond, for VHF / UHF?  

**Goals:** Understand local repeater infrastructure and how VHF / UHF radio waves propogate. 
Develop a baseline for comparing future antennas and troposcopic ducting.

Before I bought my first radio, I was concerned I wouldn't hear anything. This was largely a result of a quick google search - even from the 2nd floor of my house, it appeared I would be physically limited to repeaters within a 6 mile radius. I realized later this didn't consider factors like ground elevation and repeater height, and ultimately I've been able to work wide coverage repeaters much further than expected.

### Initial Expectation - Line of Site Calculations

The first and primary determinant for line-of-site VHF/UHF communication is based on the curvature of the earth. 
Derived from the pythagorean theorem, the equation for distance is based on the heights of the transmitting station (there's actually a lot more than that, as you'll see further on in this article):

d = 1.23 * sqrt(h)

Where d is in miles, h is in feet.

(I like this summary at [continuouswave.com](https://continuouswave.com/radio/radioHorizon.html)for explaining how this is derived). 

From a second floor window, I have about 23 feet of height, and plugging that in, I got a circle with radius 5.9 miles. Not bad, but also not great. Not enough to reach any wide area repeaters. I was certainly concerned I wouldn't be able to transmit or receive much of anything. 

### Reality 

I did read early on how the rubber duck antenna that comes with the radio is very meager, so though I wasn't ready to go with a permanent or semi-permanent antenna, I upgraded to a signal stick. 




d = 1.23( sqrt(h1) + sqrt(h2))

### Further Data Collection

At this point, I am forming a baseline with stations I can receive, as this is easier to accomplish. 

For transmission, there is the obvious question of whether a "monitoring" call out to a repeater is being heard clearly or if no one is listening or wanting to answer. Nets where viable are the way around this. 

### Results

As it turns out, I can hear much further than 6 miles away. As the map below shows, I can reach up to 40 miles away for the W1BIM repeater. Obviously this repeater being perched on top of a ___ mountain makes quite the difference! Using the line of site equation for this one, estimating a ground elevation of 1370 feet, plus a repeater height of 100 feet, we get:

d = 1.23(sqrt(1370+100) + sqrt(157+23))

= 63.6 miles. Well within range! 

Similarly for the more modestly situated 460 foot elevation W1BRI repeater in Hopkinton, MA run by the [Minuteman Repeater Association](https://mmra.org/), the calculation is:

d = 1.23(sqrt(460+100) + sqrt(157+23))

= 45 miles! 

The key is that being above the earth at all, even if only a few hundred feet, makes a very large difference. This speaks to the value of understanding how equations are derived rather than just plugging in numbers to a formula. In this case, expanding the triangle is a huge factor. 

The key thing here is that even removing the aided ability from a repeater much higher up, my base elevation was not 23 feet - it was ground elevation of 157 + 23 feet. Making my line of sight radius: 16.5 miles! This seems like an obvious point now that I've thought it through, but shows the value of thinking things through.  

if(1.23*("elevation1"*3.28084) ^ 0.5+13.41>HubDist,1,0)

### Next Steps

Now that I have inputted repeaters and topographical data into QGIS, there is an opportunity for a lot more analysis to align observations with theory. The envelope on how far I can receive is much greater than initially expected, but there is still room to investigate exactly exactly how far I can reach. There isn't generally accurate data on repeater heights, but I can do rough estimates, and use topographical data to fill in the blanks. Eventually, I'd also like to incorporate freznel zones into the analysis and use a Python package such as [pycraf] (https://github.com/bwinkel/pycraf), to incorporate the Longley-Rice / ITM propagation model. 

### Tropo Inversions
This post on Reddit from a few years ago https://www.reddit.com/r/amateurradio/comments/oumzn4/reverse_engineering_hepburn_propagation_forecast/
Hepburn propogation forcast and the anomlous ARPS signals 

## Lessons Learned
The moral of the story here is, whenever possible, go beyond blindly following equations and think about what they mean. 
However, it's also a perfect example of how many levels there are to amateur radio and why I'm so glad I fell into this hobby. 

None of these is better than any other. It's like a giant puzzle with a bunch of smaller puzzles, you can stop at any time you feel comfortable and feel good about what you're doing. But the option is always there to go deeper. 

from ITU-R P.834-4 
Ducts exist whenever the vertical refractivity gradient at a given height and location is less than−157 N/km.The existence of ducts is important because they can give rise to anomalous radiowave propagation,particularly on terrestrial or very low angle Earth-space links. Ducts provide a mechanism forradiowave signals of sufficiently high frequencies to propagate far beyond their normal line-of-sightrange, giving rise to potential interference with other services (see Recommendation ITU-R P.452).They also play an important role in the occurrence of multipath interference (see RecommendationITU-R P.530) although they are neither necessary nor sufficient for multipath propagation to occuron any particular link
