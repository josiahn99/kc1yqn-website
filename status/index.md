---
layout: default
title: Hotspot Status
---

# Hotspot Status

Current snapshot of my MMDVM Raspberry Pi 3B running Pi-Star.

<img src="../projects/pi_assembly/hotspot1.jpg" style="float: right; width: 200px;">

[Analysis of traffic]("../projects/hotspot_analysis")

[Hotspot assembly]("../projects/pi_assembly\")

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
      <center>
        <td>{{ entry.time }}</td>
      <td>{{ entry.callsign }}</td>
      <td>{{ entry.tg_slot }}</td>
      </center>
    </tr>
    {% endfor %}
  </tbody>
</table>

### System Status
<ul>
  <li>System Temp: {{ site.data.pi-star.system.temperature }}</li>
  <li>CPU Load: {{ site.data.pi-star.system.cpu_load }}</li>
  <li>Uptime: {{ site.data.pi-star.system.uptime }} </li>
  <li>Memory: {{ site.data.pi-star.system.memory }} </li>
  <li>Disk: {{ site.data.pi-star.system.disk }} </li>
</ul>
