---
layout: default
title: Programming a Codeplug
---
# Programming a Codeplug

Bottom line: The best resource I've found for determining whether you will be able to receive and transmit is the [Amateur Repeater Directory](https://amateurrepeaterdirectory.org/). Look at what you can hit and build your code plug around it! 

## How Do I Pick the Right Repeaters?
I chose the AT-878 as a first radio because of its digital and analog support, increasing the number of potential repeaters you can work. Aside from using a [digital hotspot](/projects/pi_assembly/) though, your experience with any HT is going to depend on your ability to hit nearby repeaters, and programming those repeaters into your radio via your radio's code plug (just another name for a configuration file). It's a bit of work to research, find, and program the right repeaters, but this will make the radio a lot easier to just turn on and use. 

### Understanding the importance of antenna height ###
Like any tool, it's still very useful to understand the basics of how elevation affects radio propogation.

### Repeaterbook.com ###
This website is an excellent resource for listing the repeaters in a given area, along with their frequencies. However, VHF and UHF waves are mostl dependent on line of site. Repeaterbook doesn't necessarily have information on the repeater's height,  your height, or what's between you and the repeater that might block the signal. This makes the story incomplete - why can you receive and transmit to a repeater 40 miles away, but one that is only 10 miles away is barely receivable? And how do you know if anyone is actually using the repeater? It can be very frustrating. 

### Local Repeater Resources ###

### Local Club websites ###
The direcotry has data on repeater elevations and topography, so once you provide your own elevation, it will tell you the liklihood of hitting any given repeater. 

## How do I organize the code plug? 

###

### Conclusion
Initially, I took it as a fun challenge that I was going to tackle from scratch. I downloaded topographic data for my area, researched python packages that allow for line-of-site analysis, and started the process of recording which repeaters I could transmit and receive. Utimately, while I still might do this, I found a much more efficient tool for the [Amateur Repeater Directory](https://amateurrepeaterdirectory.org/),
