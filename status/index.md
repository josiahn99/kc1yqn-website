---
layout: default
title: Hotspot Status
---

# Hotspot Status

<table class="hotspot-table">
  <thead>
    <tr>
      <th>Time (UTC)</th>
      <th>Callsign</th>
      <th>Talkgroup / Slot Info</th>
    </tr>
  </thead>
  <tbody>
    {% for entry in site.data.pi-star %}
    <tr>
      <td>{{ entry.time }}</td>
      <td>{{ entry.callsign }}</td>
      <td>{{ entry.tg_slot }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
<img src="./_data/users_by_state.jpg" alt="text" style="width:400px;">
