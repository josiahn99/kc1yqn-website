---

layout: default
title: Programming a Codeplug
-----------------------------

# Programming a Codeplug

## Bottom line

The best resource I've found for determining whether you will actually be able to receive and transmit is the Amateur Repeater Directory. Instead of starting with a generic list of repeaters, start with what you can realistically hit from your location and build your codeplug around that.

---

## How do I pick the right repeaters?

I chose the AnyTone AT-D878UVII Plus as my first radio because it supports both analog and digital modes, increasing the number of repeaters I can potentially use. In practice, though, your experience with any handheld depends almost entirely on whether you can reliably reach nearby repeaters.

That means the real work is not just finding repeaters, but confirming they are usable from where you are and then programming them into your radio’s codeplug. Once that initial effort is done, the radio becomes much easier to use day to day.

---

## Understanding the importance of antenna height

VHF and UHF communication is largely line-of-sight, which makes antenna height far more important than most beginners expect. A repeater that is dozens of miles away but mounted high on a tower or hill can be easier to reach than one much closer but blocked by terrain or buildings.

A common starting point for VHF/UHF propagation is the radio horizon formula:

d = 1.23 (√h₁ + √h₂)

Where:

* d = distance in miles
* h₁, h₂ = antenna heights in feet

This is why distance alone is a poor indicator of whether a repeater will work. What matters is the combination of your height, the repeater’s height, and everything in between.

---

## RepeaterBook

RepeaterBook is usually the first place to look. It provides frequencies, offsets, tones, and a broad list of repeaters in your area, which makes it extremely useful for initial discovery.

However, it doesn’t tell the full story. It generally won’t indicate whether a repeater is active, how often it’s used, or whether your specific location can reach it reliably. It answers the question “what exists,” but not “what will work for me.”

---

## Amateur Repeater Directory

The Amateur Repeater Directory fills in many of those gaps by incorporating elevation and terrain data. After entering your location, it can estimate how likely you are to reach a given repeater based on line-of-sight and topography.

This makes it much more practical for building a usable codeplug, because it shifts your focus from theoretical coverage to real-world probability.

---

## Local repeater resources

Local club websites tend to have the most up-to-date information about which repeaters are active and when people are actually on the air. A repeater you can technically reach but nobody uses is not very helpful when you’re starting out.

Listening for scheduled nets or checking club pages can quickly point you toward repeaters that will give you actual operating experience.

---

## How do I organize the codeplug?

Once you’ve identified repeaters that are both reachable and active, organization becomes important. The goal is to make the radio intuitive to use rather than a long list of channels you have to scroll through.

I’ve grouped my channels into the following categories (zones on the AT-878):

* **Local Analog**
  A focused list (10–15) of repeaters I can reliably hit and that have at least occasional activity.

* **Local Digital**
  Separate channels for each talkgroup on the same repeater.

* **DMR Hotspot**
  Channels dedicated to hotspot use.

* **Regional**
  Additional VHF/UHF repeaters within roughly a 50-mile radius.

* **Travel**
  Repeaters in areas I visit periodically.

Clear naming also makes a big difference. Labeling channels by location or club name is far more useful than leaving default or cryptic labels.

The resources above aren’t perfect. If a repeater should be within range but isn’t working, double-check frequency, offset, and PL/DCS tones from RepeaterBook. A small mistake here can completely prevent access—I ran into this myself and it was surprisingly frustrating until corrected.

Over time, refine your codeplug based on what you actually use rather than trying to include everything upfront. In the few months I’ve had my HT, I’ve already gone through several iterations. Don’t hesitate to rebuild it from scratch if it’s not working well.

---

## Conclusion

Initially, I approached this as a technical problem to solve from scratch. I experimented with topographic data, looked into Python tools for line-of-sight analysis, and started mapping which repeaters I could reach.

While that approach is still interesting, it quickly became clear that better tools already exist. I may revisit the deeper technical side of VHF propagation later, but for now the Amateur Repeater Directory provides a much faster and more practical way to identify usable repeaters without reinventing the process.

The key takeaway is simple:

**Don’t build your codeplug from a list of repeaters—build it from the ones you can actually use.**
