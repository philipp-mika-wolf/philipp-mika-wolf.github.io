---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
---

## Conference Talks

- *2025* – “test 1” at **LEIS workshop**, Uppsala, Sweden
- *2024* – “test 2” at **HRDP**, Dresden, Germany
- *2024* – “test 3” at **IBMM**, London, United Kingdom

## Conference Locations Map

<div id="map" style="height: 500px;"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
  var map = L.map('map').setView([20,0], 2); // World view

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
  }).addTo(map);

  // Add markers for each talk
  var talks = [
    { title: "test 1", event: "LEIS workshop", location: "Uppsala, Sweden", coords: [59.837510, 17.647830] },
    { title: "test 2", event: "HRDP", location: "Dresden, Germany", coords: [51.062429, 13.950421] },
    { title: "test 3", event: "IBMM", location: "London, UK", coords: [51.522993, -0.040866] }
  ];

  talks.forEach(function(talk) {
    L.marker(talk.coords).addTo(map)
      .bindPopup("<b>" + talk.title + "</b><br/>" + talk.event + "<br/>" + talk.location);
  });
</script>
