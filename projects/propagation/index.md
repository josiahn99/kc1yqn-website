---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

### Summary
Question: What kind of propogation can I expect, under normal conditions and beyond, for VHF / UHF?  

Even before I bought an HT, a major concern about getting into amateur radio was whether I would be able to hear anything on VHF from my current living situation. In the suburbs, simplex didn't seem like a likely route to making contacts, so it became a question of repeaters. There aren't many repeaters within my 6-mile line-of-sight circle, so my expectations were low. 

As it turns out, my initial guess didn't incorporate topography or repeater height, which play a major role in being able to reach much, much further than expected, which leads to opportunities to conduct further analysis that algin the observations with theory. 

### Initial Expectation - Line of Site Calculations

The first and primary determinant for line of site VHF/UHF communication is based on the curvature of the earth. 
Derived from the pythagorean theorem, the equation for distance is based on the heights of the transmitting and receiving stations, h1 and h2:

d = 1.23( sqrt(h1) + sqrt(h2))

Where d is in miles, h1 and h2 are in feet. 

(I like this summary at [continuouswave.com] (https://continuouswave.com/radio/radioHorizon.html) for explaining how this is derived). 

From a second floor window, I have about 23 feet of height from the top of my slim jim antenna. Plugging this into the formula, you get about a circle with radius 5.9 miles. Not bad, but also not great. Not enough to reach any wide area repeaters. I was certainly concerned I wouldn't be able to transmit or receive much of anything. This is a large reason I went into buying my first HT with meager expectations and hedged my bets by buying a DMR capable radio with a DMR hotspot. 

### Observations

As it turns out, 

### Next Steps

Now that I have inputted repeaters and topographical data into QGIS, there is an opportunity for a lot more analysis to align observations with theory. There isn't generally accurate data on repeater heights, but I can do rough estimates, and use topographical data to fill in the blanks. Eventually, I'd also like to incorporate freznel zones into the analysis and use the python package [pycraf] (https://github.com/bwinkel/pycraf), that incorporate the Longley-Rice / ITM propagation model. 
