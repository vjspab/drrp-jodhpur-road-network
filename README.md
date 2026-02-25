# 🗺️ DRRP Jodhpur — Road Network GIS Dataset

> **Draft Revised Regional Plan (DRRP) — Jodhpur District, Rajasthan**
> Road network dataset in KML format for GIS analysis, transport planning, and regional development studies.

[![Format](https://img.shields.io/badge/Format-KML%20%2F%20GIS-blue?logo=googlemaps)](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)
[![District](https://img.shields.io/badge/District-Jodhpur-orange)](https://en.wikipedia.org/wiki/Jodhpur_district)
[![State](https://img.shields.io/badge/State-Rajasthan-green)](https://en.wikipedia.org/wiki/Rajasthan)
[![Records](https://img.shields.io/badge/Road%20Segments-2%2C346-red)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

---

## 📋 Overview

This repository contains the **DRRP (Draft Revised Regional Plan) road network dataset for Jodhpur District, Rajasthan**, published as part of regional transport infrastructure planning. The data is provided in **KML (Keyhole Markup Language)** format and is compatible with Google Earth, QGIS, ArcGIS, and other GIS tools.

### Key Facts

| Attribute | Value |
|-----------|-------|
| **Document ID** | `DRRP_Jodhpur` |
| **State** | Rajasthan (State ID: 29) |
| **District** | Jodhpur (District ID: 260) |
| **Total Road Segments** | **2,346 Placemarks** |
| **Geometry Type** | `LineString` / `MultiGeometry` |
| **Coordinate System** | WGS 84 (EPSG:4326) — Longitude/Latitude |
| **File Size** | ~13.5 MB |
| **KML Standard** | OGC KML 2.2 |
| **Road Authority** | PWD (Public Works Department), Rajasthan |

---

## 📦 Dataset Contents

### File

| File | Description |
|------|-------------|
| [`DRRP_Jodhpur.kml`](DRRP_Jodhpur.kml) | Full road network KML dataset for Jodhpur district |

### Attribute Fields

Each road Placemark contains the following attributes in its description popup:

| Field | Description | Example |
|-------|-------------|---------|
| `FID` | Feature ID (sequential) | `0`, `1`, `2`... |
| `ER_ID` | Unique Road Entity ID | `1146703` |
| `Shape_Leng` | Shape length in degrees | `0.03234` |
| `Road_Cat` | Road Category code | `VR`, `MDR`, `NH`, `SH` |
| `Road_Code` | Unique road code | `RR(VR)2219`, `VR0842` |
| `Road_Owner` | Owning authority | `PWD` |
| `SN` | Serial Number | `29691` |
| `State_Id` | State numeric ID | `29` |
| `State_Name` | State name | `Rajasthan` |
| `Distt_Id` | District numeric ID | `260` |
| `Distt_Name` | District name | `Jodhpur` |
| `Block_Id` | Administrative block ID | `449` |
| `Block_Name` | Administrative block name | `Balesar` |
| `ER_ID_1` | Road entity reference ID | `1146703` |
| `ER_Code` | Road entity code | `RR(VR)2219` |
| `Length` | Road length in km | `4` |
| `Road__Name` | Road name / description | `AR to Mahasati Nagar` |
| `Category` | Full road category name | `Rural Road(Village Roads)` |

### Road Categories

| Code | Full Name |
|------|-----------|
| `VR` | Village Road |
| `MDR` | Major District Road |
| `ODR` | Other District Road |
| `SH` | State Highway |
| `NH` | National Highway |

---

## 🗺️ How to Open / Use

### Google Earth (Desktop or Web)
1. Download [`DRRP_Jodhpur.kml`](DRRP_Jodhpur.kml)
2. Double-click the file — it will open directly in Google Earth
3. Or drag-and-drop into [Google Earth Web](https://earth.google.com/web/)

### QGIS (Free & Open Source GIS)
1. Open QGIS → `Layer → Add Layer → Add Vector Layer`
2. Select the `.kml` file
3. Or drag-and-drop the file into the QGIS window
4. The road network will render with all attribute data available in the attribute table

### ArcGIS
1. Use `Add Data → Add Basemap` or `KML to Layer` geoprocessing tool
2. Or simply drag-and-drop the `.kml` file into ArcMap/ArcGIS Pro

### Python (GeoPandas)
```python
import geopandas as gpd

# Load the KML file
gdf = gpd.read_file("DRRP_Jodhpur.kml", driver="KML")

# Explore the data
print(gdf.shape)          # Number of road segments
print(gdf.columns)        # Available columns
print(gdf.crs)            # Coordinate reference system
gdf.plot()                # Quick visual plot
```

### Converting to GeoJSON / Shapefile
```bash
# Using ogr2ogr (GDAL)
# Convert to GeoJSON
ogr2ogr -f GeoJSON output.geojson DRRP_Jodhpur.kml

# Convert to Shapefile
ogr2ogr -f "ESRI Shapefile" output_shapefile/ DRRP_Jodhpur.kml
```

---

## 📍 Spatial Coverage

The dataset covers the **Jodhpur District** of Rajasthan, India, including multiple administrative blocks such as:
- Balesar
- And other blocks across Jodhpur district

**Approximate Bounding Box:**
- Longitude: ~72.4° E to ~73.0° E
- Latitude: ~26.5° N to ~27.0° N

---

## 🏗️ About DRRP

The **Draft Revised Regional Plan (DRRP)** is a statutory planning document prepared by the **Rajasthan Urban Improvement Trust (UIT) / JDA (Jodhpur Development Authority)** under the Rajasthan Urban Improvement Trust Act. It defines land use, road network, infrastructure, and development zones for the Jodhpur region.

This road network layer captures the existing and proposed road hierarchy as part of the regional transport planning framework.

---

## 🔗 Related GIS Resources

- [Jodhpur Development Authority](https://jda.rajasthan.gov.in/)
- [QGIS Download](https://qgis.org/)
- [Google Earth](https://earth.google.com/)
- [OGC KML Standard](https://www.ogc.org/standard/kml/)
- [GDAL/OGR Tools](https://gdal.org/)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

The GIS dataset is derived from the **Draft Revised Regional Plan, Jodhpur** and is intended for research, planning, and educational use.

---

## 👤 Maintained By

**Vijay** — Urban & Transport Planner | GIS & Spatial Data Enthusiast

> *Part of a collection of GIS datasets and planning tools for urban and regional development in Rajasthan.*
