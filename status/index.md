---
layout: default
title: Hotspot Status
---

# Hotspot Status

Current snapshot of my MMDVM Raspberry Pi 3B running Pi-Star.

Check [here]("..\projects\hotspot_analysis\") for an analysis of traffic.

### Recently Heard

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
      <td>{{ entry.callsign }}</td>
      <td>{{ entry.tg_slot }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

### System Status
System Temp: {{ site.data.pi-star.system.temperature }}
CPU Load: {{ site.data.pi-star.system.cpu_load }}
    

<img src="../assets/images/users_by_state.jpg" width="400">

