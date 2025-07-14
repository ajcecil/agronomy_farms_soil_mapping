# Iowa State Agronomy Farm Soil Mapping

Map Documentation

## Contents

- [Datastore](https://iastate.app.box.com/folder/330408802946?s=ytjl7nqkroxs3haodak27xjpkaqpajh4)


# Map Data
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script src="https://unpkg.com/geotiff/dist/geotiff.browser.min.js"></script>
<script src="https://unpkg.com/leaflet-geotiff/dist/leaflet-geotiff.min.js"></script>
<script src="https://unpkg.com/leaflet-geotiff/dist/leaflet-geotiff-plotty.min.js"></script>



<div id="map" style="height: 500px;"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    var map = L.map('map').setView([0, 0], 2); // placeholder

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    // Load GeoTIFF
    var layer = new L.LeafletGeotiff('https://drive.google.com/file/d/1_EBpzMxXie6MROXYhQlBIqCeE57DoksO/', {
      renderer: new L.LeafletGeotiff.Plotty({
        displayMin: 0,
        displayMax: 255,
        colorScale: 'viridis',
      }),
      onReady: function () {
        // Zoom to bounds once the raster loads
        map.fitBounds(this.getBounds());
      }
    }).addTo(map);
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