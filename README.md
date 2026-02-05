![Screenshot](https://img.shields.io/badge/zero--config-single%20HTML%20file-blue)
# 📍 GeoJSON Map Viewer

A lightweight, single-file HTML tool to visualize location data from JSON files on an interactive map. Just drag & drop your file — no server, no install, no dependencies to manage.

<img width="1921" height="957" alt="image" src="https://github.com/user-attachments/assets/ab4a7919-2e44-42be-965a-c1db4022ad87" />

## Features

- **Drag & drop** — drop a JSON file and instantly see your locations on a map
- **Flexible JSON parsing** — supports multiple coordinate formats (see below)
- **Marker clustering** — handles thousands of points with smooth clustering
- **Coverage stats** — shows total locations and geographic spread
- **Zero install** — single HTML file, opens in any browser
- **Responsive** — works on desktop and mobile

## Usage

1. Download or clone `geojson-map-viewer.html`
2. Open it in your browser
3. Drop a JSON file containing location data

That's it.

## Supported JSON Formats

The viewer auto-detects coordinates from many common structures:

```json
// Flat coordinates
[{ "lat": 48.8566, "lng": 2.3522 }]
[{ "latitude": 48.8566, "longitude": 2.3522 }]

// Nested objects
[{ "geolocation": { "latitude": 48.8566, "longitude": 2.3522 } }]
[{ "Geolocation": { "lat": 48.8566, "lng": 2.3522 } }]
[{ "coordinates": { "lat": 48.8566, "lng": 2.3522 } }]
[{ "position": { "latitude": 48.8566, "longitude": 2.3522 } }]

// GeoJSON Features
[{ "geometry": { "coordinates": [2.3522, 48.8566] }, "properties": { "name": "Paris" } }]
```

Optional fields: `name`, `title`, `label`, `id` — displayed in the marker popup.

## Customization

Edit the CSS variables at the top of the file to match your brand:

```css
:root {
  --app-primary: #0057FF;
  --app-primary-dark: #0042C6;
  --app-accent: #00E5A0;
  --app-bg: #F6F8FC;
  --app-surface: #FFFFFF;
  --app-text: #1A1F36;
  --app-text-muted: #6B7394;
  --app-border: #E2E6F0;
  --app-radius: 14px;
}
```

## Built With

- [Leaflet](https://leafletjs.com/) — interactive maps
- [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) — marker clustering
- [CARTO](https://carto.com/) — basemap tiles

## License

MIT — use it however you want.
