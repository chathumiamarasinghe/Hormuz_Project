# 🌊 Strategic Location of the Strait of Hormuz — GIS Project

> **GIS Practical Assignment** | Why Geography Matters: Mapping Strategic Importance of Countries  
> **Topic:** Strategic Location of the Strait of Hormuz  
> **Tool:** QGIS  
> **Date:** April 2026

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Data Sources](#data-sources)
- [Maps Created](#maps-created)
- [References](#references)

---

## 📌 Project Overview

This project uses **GIS (Geographic Information System)** tools to analyse why the **Strait of Hormuz** is one of the most strategically important geographic locations on Earth.

The Strait of Hormuz is a narrow waterway (~33 km wide at its narrowest point) located between **Iran** (north) and **Oman/UAE** (south). It is the **only maritime exit** from the Persian Gulf, through which approximately **21% of global oil trade** passes every day.

### Research Questions Answered

| # | Question | Answer (Summary) |
|---|----------|-----------------|
| 1 | Why is this region important? | Only exit point from Persian Gulf all energy exports pass through here |
| 2 | What natural resources does it have? | World's largest concentration of oil & gas reserves |
| 3 | Does location affect trade? | Directly geography forces all tankers through one 3 km channel |
| 4 | Are there strategic features? | Narrow channel, competing borders, major ports, no alternative route |

---


## 📁 Repository Structure

```
Hormuz_GIS_Project/
│
├── README.md                        ← This file
│
├── Data/                            ← All downloaded GIS data
│   ├── 
│   │   ├── ne_10m_admin_0_countries.shp     ← Country boundaries
│   │   ├── ne_10m_admin_0_countries.dbf
│   │   ├── ne_10m_admin_0_countries.prj
│   │   └── ne_10m_admin_0_countries.shx
│   │   ├── IRN_coastlines.shp               ← Iran coastline
│   │   ├── OMN_coastlines.shp               ← Oman coastline
│   │   ├── IRN_rivers.shp                   ← Iran rivers
│   │   ├── OMN_rivers.shp                   ← Oman rivers
│   │   ├── IRN_ports.shp                    ← Iran ports
│   │   ├── OMN_ports.shp                    ← Oman ports
│   │   ├── IRN_population.tif               ← Iran population raster
│   │   ├── OMN_population.tif               ← Oman population raster
│   │   ├── IRN_elevation.tif                ← Iran elevation raster
│       └── OMN_elevation.tif                ← Oman elevation raster
|
├── QGIS/
│   └── Hormuz_Map.qgz                       ← Main QGIS project file (open this)
│
├── Maps/                            ← Exported map images (300 DPI)
│   ├── Map1_Political.png
│   ├── Map2_Resources.png
│   ├── Map3_Shipping.png
    └── Map4_Population.png

```

---

## 🗂️ Data Sources

All data used in this project is **free and publicly available** from reliable academic and government sources.

### 1. Country Boundaries & Coastlines
| Item | Source | URL | Format | License |
|------|--------|-----|--------|---------|
| Country boundaries | Natural Earth | [naturalearthdata.com](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/) | `.shp` | Public Domain |
| Coastlines | Natural Earth | [naturalearthdata.com](https://www.naturalearthdata.com/downloads/10m-physical-vectors/) | `.shp` | Public Domain |


---

### 2. Administrative Boundaries, Rivers, Ports, Population, Elevation
| Item | Country | Source | URL | Format |
|------|---------|--------|-----|--------|
| Coastlines | Iran + Oman | DIVA-GIS | [diva-gis.org/gdata](https://www.diva-gis.org/gdata) | `.shp` |
| Rivers | Iran + Oman | DIVA-GIS | [diva-gis.org/gdata](https://www.diva-gis.org/gdata) | `.shp` |
| Ports | Iran + Oman | DIVA-GIS | [diva-gis.org/gdata](https://www.diva-gis.org/gdata) | `.shp` |
| Population density | Iran + Oman | DIVA-GIS | [diva-gis.org/gdata](https://www.diva-gis.org/gdata) | `.tif` |
| Elevation / terrain | Iran + Oman | DIVA-GIS | [diva-gis.org/gdata](https://www.diva-gis.org/gdata) | `.tif` |


---

## 🗺️ Maps Created

All maps were created in **QGIS 3.x** using the Print Layout tool and exported at **300 DPI**.

### Map 1 — Political Map
- **Layers used:** Country boundaries, coastlines, rivers, ports
- **Styling:** Categorized country fill colors, blue water, dark border lines
- **Shows:** Political geography of the Strait — which country controls which shore
- **File:** `Maps/Map1_Political.png`

### Map 2 — Resource Map (Oil & Gas)
- **Layers used:** Country boundaries (outline only), oil & gas CSV points
- **Styling:** Categorized by fuel type — red = oil, orange = gas
- **Shows:** Concentration of energy resources surrounding the Persian Gulf
- **File:** `Maps/Map2_Resources.png`

### Map 3 — Shipping / Trade Routes Map
- **Layers used:** Coastlines, country boundaries, ports, digitized shipping lanes
- **Styling:** Blue dashed lines for shipping lanes, red dots for ports
- **Shows:** How all maritime trade funnels through the Strait chokepoint
- **File:** `Maps/Map3_Shipping.png`

### Map 4 — Population Distribution Map
- **Layers used:** Iran + Oman population raster (merged), Iran + Oman elevation raster, country boundaries
- **Styling:** YlOrRd color ramp (yellow = low density, dark red = high density)
- **Raster merge:** Raster → Miscellaneous → Merge (Iran + Oman combined)
- **Shows:** Coastal population concentration and desert interior
- **File:** `Maps/Map4_Population.png`

---



## 📚 References

| Source | Type | URL |
|--------|------|-----|
| U.S. Energy Information Administration | Statistical data | https://www.eia.gov/international/analysis/special-topics/World_Oil_Transit_Chokepoints |
| Natural Earth | GIS data | https://www.naturalearthdata.com |
| DIVA-GIS | GIS data | https://www.diva-gis.org |
| Global Energy Monitor | Oil & gas data | https://globalenergymonitor.org |
| IMO Traffic Separation Scheme | Navigation data | https://www.imo.org |
| International Energy Agency | Energy statistics | https://www.iea.org |
| QGIS Documentation | Software | https://docs.qgis.org |

---


*Created with QGIS 3.x | Data from Natural Earth, DIVA-GIS, Global Energy Monitor | April 2026*
