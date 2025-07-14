# Iowa State Agronomy Farm Soil Mapping

Map Documentation

## Contents

- [Datastore](https://iastate.app.box.com/folder/330408802946?s=ytjl7nqkroxs3haodak27xjpkaqpajh4)


# Map Data

<!-- Keep only Leaflet core -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<div id="map" style="height: 500px;"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    var map = L.map('map').setView([41.5, -94.0], 8); // Initial view

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    // Image overlay
    var imageUrl = 'https://your-username.github.io/your-repo/docs/page_files/aoi_rgb.png';
    var imageBounds = [[41.0000, -94.5000], [42.0000, -93.5000]];

    L.imageOverlay(imageUrl, imageBounds).addTo(map);
    map.fitBounds(imageBounds);
  });
</script>


## Soil Properties

### pH

### Base pH

### Organic Matter 

### Phosphorus (Melich 3)

### Potassium

### Sulfur

### Cation Exchange Capacity

### Calcium

### Magnesium

### H_SAT

### K_SAT

### MG_SAT

### CA_SAT