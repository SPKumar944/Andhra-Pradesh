# Andhra Pradesh Smart Land & Infrastructure Governance Dashboard (Task AGT-93)

[![Live Dashboard](https://img.shields.io/badge/Live-Public%20Dashboard-emerald?style=for-the-badge&logo=github)](https://spkumar944.github.io/Andhra-Pradesh/)
[![Coordinate System](https://img.shields.io/badge/CRS-EPSG%3A4326%20%2F%20EPSG%3A32643-blue?style=for-the-badge)](https://epsg.io/32643)
[![License](https://img.shields.io/badge/License-Government%20Cadastral%20Data-amber?style=for-the-badge)](#)

Interactive Cadastral GIS & Land Governance Web Application for **N Thimmapuram Village** (Vemulapadu Gram Panchayat, Yadiki Mandal, Anantapur District, Andhra Pradesh) and infrastructure networks for **Anantapuram Ward 6**.

🔗 **Public Live Web Dashboard:** [https://spkumar944.github.io/Andhra-Pradesh/](https://spkumar944.github.io/Andhra-Pradesh/)

---

## 🗺️ GIS Layers & Converted Datasets

All raw CAD drawings, drone GeoPDFs, and cadastral survey registers have been converted into production-ready **GeoJSON format (EPSG:4326 - WGS 84)**:

| File Name | Features | Geometry | Description |
| :--- | :---: | :---: | :--- |
| [`N_Thimmapuram_Cadastral_Parcels.geojson`](./N_Thimmapuram_Cadastral_Parcels.geojson) | **104** | Polygon | All 104 surveyed cadastral plots with **45 revenue columns populated** (Owner names, Aadhaar, father/husband names, building classifications, extent, plinth area, neighbor adjacencies, legal tenure). |
| [`N_Thimmapuram_Builtup_Structures.geojson`](./N_Thimmapuram_Builtup_Structures.geojson) | **61** | Polygon | Building footprints with spatial join to parent parcel, plinth areas, and RCC vs. Non-RCC classifications. |
| [`N_Thimmapuram_Roads.geojson`](./N_Thimmapuram_Roads.geojson) | **11** | LineString | Village boundary roads, interior streets, and pathway alignments. |
| [`Anantapuram_Ward6_Road_Network.geojson`](./Anantapuram_Ward6_Road_Network.geojson) | **31** | Polygon | Road network corridors and street segments for Revenue Colony, Ramachandra Nagar, and Shirdinagar. |
| [`Anantapuram_Ward6_Stormwater_Drains.geojson`](./Anantapuram_Ward6_Stormwater_Drains.geojson) | **25** | LineString | Stormwater drainage network classified into covered stormwater drains and primary arterial drains. |

---

## 📊 Village Baseline Metrics (N Thimmapuram)

* **Settlement Area:** 8.19 Acres (33,149 m²)
* **Total Property Records:** 104 records
* **Residential Records:** 52 records (50 private individual records)
* **Demographics:** 145 population, 45 households
* **Drinking Water:** 45 functional household tap connections (100% village coverage)
* **Building Types:** 10 RCC Pucca buildings, 37 Non-RCC structures, 57 vacant land records
* **Female Property Titles:** 12 properties (1,028 m² inherited)
* **Shortlisted Govt Land:** 2.08 Acres across 6 plots (~42 housing sites of 200 m² potential)

---

## 🚀 Dashboard Features

1. **Interactive Cadastral Map:** Hardware-accelerated SVG GIS viewer supporting Pan, Zoom, and Layer toggling.
2. **Click-to-Inspect:** Click any parcel to view all 45 official revenue attributes in the sidebar inspector.
3. **Filter Chips:** Instant filtering by Property Category (Residential, RCC, Non-RCC, Vacant Land, Female Owned).
4. **Searchable Register:** Searchable table of all 104 properties with real-time text matching.
5. **One-Click CSV Export:** Export the complete reconciled cadastral register to CSV.
6. **File Prologue & Inventory:** Exhaustive catalogue of all raw CAD drawings, PDFs, and master deliverables.

---

## 🛠️ Usage in GIS Software

You can load these GeoJSON files directly into:
* **QGIS / ArcGIS Pro:** `Layer` → `Add Layer` → `Add Vector Layer...`
* **Google Earth Web:** `New Project` → `Import KML / GeoJSON file`
* **Web Maps (Leaflet, Mapbox, OpenLayers):** Load natively via standard GeoJSON fetch.

```javascript
fetch('N_Thimmapuram_Cadastral_Parcels.geojson')
  .then(res => res.json())
  .then(data => L.geoJSON(data).addTo(map));
```
