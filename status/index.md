---
layout: default
title: Hotspot Status
---

# Hotspot Status

Current snapshot of my MMDVM Raspberry Pi 3B running Pi-Star.

<img src="/projects/pi_assembly/hotspot4.jpg" style="float: right; width: 200px;">

[Analysis of traffic]("/projects/hotspot_analysis/")

[Hotspot assembly]("/projects/pi_assembly/")

### Recent Traffic

<table class="hotspot-table">
  <thead>
    <tr>
      <th>Time (UTC)</th>
      <th>Callsign</th>
      <th>Talkgroup / Slot Info</th>
    </tr>
  </thead>
  <tbody>
    {% for entry in site.data.pi-star.entries %}
    <tr>
      <td>{{ entry.time }}</td>
      <td><center>{{ entry.callsign }}</center></td>
      <td><center>{{ entry.tg_slot }}</center></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

### System Status
<ul>
  <li><b>System Temp:</b> {{ site.data.pi-star.system.temperature }}</li>
  <li><b>CPU Load:</b> {{ site.data.pi-star.system.cpu_load }}</li>
  <li><b>Uptime:</b> {{ site.data.pi-star.system.uptime }} </li>
  <li><b>Memory:</b> {{ site.data.pi-star.system.memory }} </li>
  <li><b>Disk:</b> {{ site.data.pi-star.system.disk }} </li>
</ul>
