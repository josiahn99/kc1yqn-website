---
layout: default
title:  Propagation Analysis
---
# VHF / UHF Propagation Analysis

### Summary
**Question:** What kind of propogation can I expect, under normal conditions and beyond, for VHF / UHF?  

Even before I bought an HT, a major concern about getting into amateur radio was whether I would be able to hear anything on VHF from my current living situation. In the suburbs, simplex didn't seem like a likely route to making contacts, so it became a question of repeaters. There aren't many repeaters within my 6-mile line-of-sight circle, so my expectations were low. 

As it turns out, my initial guess didn't incorporate topopgraphy or repeater height, which play a major role in being able to reach much, much further than expected, which leads to opportunities to conduct further analysis that algin the observations with theory. 

** Key Conclusion **: Ground elevation is part of your antenna height, too. Don't blindly trust the equations. Think about how they are derived.

### Initial Expectation - Line of Site Calculations

The first and primary determinant for line of site VHF/UHF communication is based on the curvature of the earth. 
Derived from the pythagorean theorem, the equation for distance is based on the heights of the transmitting and receiving stations, h1 and h2:

d = 1.23( sqrt(h1) + sqrt(h2))

Where d is in miles, h1 and h2 are in feet. 

(I like this summary at [continuouswave.com](https://continuouswave.com/radio/radioHorizon.html)for explaining how this is derived). 

From a second floor window, I have about 23 feet of height from the top of my slim jim antenna. Plugging this into the formula, you get about a circle with radius 5.9 miles. Not bad, but also not great. Not enough to reach any wide area repeaters. I was certainly concerned I wouldn't be able to transmit or receive much of anything. This is a large reason I went into buying my first HT with meager expectations and hedged my bets by buying a DMR capable radio with a DMR hotspot. 

### Data Collection

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

Now that I have inputted repeaters and topographical data into QGIS, there is an opportunity for a lot more analysis to align observations with theory. The envelope on how far I can receive is much greater than initially expected, but there is still room to investigate exactly exactly how far I can reach. There isn't generally accurate data on repeater heights, but I can do rough estimates, and use topographical data to fill in the blanks. Eventually, I'd also like to incorporate freznel zones into the analysis and use the python package [pycraf] (https://github.com/bwinkel/pycraf), that incorporate the Longley-Rice / ITM propagation model. 
