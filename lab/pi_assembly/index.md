---
layout: default
title: Pi Hotspot Assembly
---

<div class="project-summary">

**Project:** Raspberry Pi DMR Hotspot  
**Time to Assemble:** ~1 hour  
**Skill Level:** Beginner  
**Total Cost:** ~$110–150  

**Key Components**

- Raspberry Pi 3  
- MMDVM hotspot board  
- microSD card  
- 5V power supply  
- Case  

</div>

# Purpose 

One of my initial concerns with getting my tech license and a VHF/UHF handheld trnaceiver was that I wouldnt' ahve any repeaters in range and everything would be silent. I considered a DMR hotspot to be a key fall back that would allow me to make QSOs off the bat, no matter what. In my experience it doesn't carry the no-infrastructure magic of non internet related stations, but it makes sure that you can always talk to someone and get practice being on the air, day or night, without having to wait for nightly nets once a week or just calling "listening" into a local repeater. As it turns out, the hotspot has also given me an opening into learning basic Linux and web hosting, but that's for another article.

## Equipment

There are many pre-built hotspots available, but in the DIY spirit I decided to go the route of assembling mine. The ingredients were:

- MMDVM hotspot https://www.amazon.com/dp/B0BP6ZYF18. You can buy a simplex (1 antenna) or duplex (2 attennas). The online consensus seemed to be that the simplex was simpler and would accomplish most of my needs, so I didn't spent too much time beyond that researching. Some have an OLED screen, which I haven't found that useful, but does look cooler if you go with the see-through case. 


- Raspberry Pi. Finally a reason a hobby that gives me a reason to buy one and have a purpose! After much deliberation I went with the Pi 3 which seemed like a sweet spot between processing power and power / cooling needs. The Pi-Zero will do the job, though if you want a bit more flexibility to do anything else beyond just hotspotting, like running Python scripts, it seems like the 3 is a better call. One thing to note if you buy on Amazon, check what your Pi comes with - mine did not come with a 5V power adapter so I had to buy that separately, and you will need a micro SD card as well. If you don't want to sodder,buy the pi with the hat that the MMDVM sits on already installed. 

- Case. I bought a pretty little case from C4 labs. Non see through will work just fine, but I liked the style points.  https://www.amazon.com/dp/B07MQBYLGW?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1

Assembling the pi, hotspot, and case was a fun little project. Everything went together easily and it took about an hour. With no soldering, it was an assembly not a build, but the directions in the C4 labs case were straightforward in a lego or Ikea way. I was very happy with the end result:
 

## Pi-Star Set Up
Pi-Star is a software image built specifically for Raspberry Pi DMR hotspots, rather than the standard Pi OS. There are loads of youtube videos that go through the process of flashing Pi-Star to your Pi and setting it up, so I won't get into that here. The ones I found helpful were ___ 

The only thing that wasn't straightforward was the need to add a 01 to your DMR ID (which you will need to register for here). This seemed to be overlooked in most online materials.

## Operation
So far I've really just explored 3100 USA TG, 93 North America, and 91 Worldwide. Worldwide is a constant stream of QSOs, the trick there is listening to a QSO and being ready to pounce on the PTT once it is over for your turn. A much easier way to make international QSOs is 93 North America, which has a lot of non-North Americans on it, and is far less busy so you don't have to be quite so quick. 3100 USA seems to be a bit more quiet but still usually someone will respond if you put a call out there.

## Conclusions
The hotspot has really accomplished just what I wanted it to. There's always someone to hear and communicate with on your radio. It's a huge plus when you're getting into the hobby that you can do it without having to spend money on a more expensive mobile or HF rig, or set up a large antenna. Does it have the same magic? No. Does the sound quality and ease make it feel a bit like just using the internet? Yes. But it's a great compromise. 

The other thing that's great is that having a reason to finally buy a Raspberry Pi, I have been able to use it as a way to play around with my other interests, like Python and data analysis. While Pi-Star doesn't automatically store too much data about calls or talk groups, it is certainly enough of a datasource to do some fun things with and makes me all the more likely to buy another Pi soon. 

