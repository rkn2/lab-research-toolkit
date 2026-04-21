# Finding Data

Good research often depends on finding the right dataset before you can answer your question. This guide covers the main data sources relevant to the lab's work — natural hazards, historic structures, and geospatial data.

---

## Natural Hazards Data

### DesignSafe-CI (NHERI)
**designsafe-ci.org**

The National Science Foundation's data repository for natural hazards engineering research. This is the first place to look for datasets related to earthquakes, hurricanes, tornadoes, floods, and other hazard events. Researchers who receive NSF funding are often required to deposit their data here, so it contains a large and growing collection of curated, citable datasets.

- Search by hazard type, structure type, or keyword
- Data includes field reconnaissance, sensor data, simulation results, and more
- Datasets are citable — you can reference them in papers the same way you would reference a publication

### FEMA National Flood Hazard Layer
**msc.fema.gov** and available as a GIS layer

FEMA's flood maps show 100-year and 500-year flood zones for the entire United States. Useful for understanding flood exposure of buildings in your study area. Available as a downloadable GIS layer or through the FEMA Map Service Center.

### NOAA Storm Events Database
**ncdc.noaa.gov/stormevents**

Historical records of tornado tracks, flood events, hail, and other severe weather going back decades. Useful for identifying which areas experienced specific hazard events and for ground-truthing damage data.

### Tornado Probability and Track Data
The Storm Prediction Center (SPC) at NOAA maintains historical tornado track data as a GIS layer:
- **SPC GIS data:** spc.noaa.gov/gis/svrgis — download tornado, hail, and wind tracks as shapefiles
- Useful for probabilistic risk mapping and for identifying buildings that experienced known tornado events

---

## Historic Structures Data

### National Register of Historic Places
**nps.gov/subjects/nationalregister**

The official federal list of historic properties in the United States. Maintained by the National Park Service. Useful for:

- Identifying historic buildings and districts in a study area
- Accessing nomination forms, which often contain detailed documentation of building age, construction type, and significance
- Downloadable as a database with location and basic attribute information

The full database is available from the NPS and is also accessible through state historic preservation offices (SHPOs), which often have more detailed local data.

### State Historic Preservation Offices (SHPOs)
Each state maintains its own inventory of historic properties, often with more detail than the national register. Pennsylvania's is maintained by PHMC (phmc.pa.gov). If you are working on a Pennsylvania-focused project, PHMC data is worth checking.

---

## Geospatial and Building Stock Data

### OpenStreetMap
**openstreetmap.org** and downloadable via tools like Overpass Turbo

A global, community-maintained map database. Building footprints, road networks, and land use data are available for most of the world. Quality varies by location but is generally good for urban areas in the US and Europe. Useful as a base layer and for building stock analysis.

### Microsoft Building Footprints
Microsoft has released building footprint datasets for the US and other countries, derived from satellite imagery using computer vision. More complete than OpenStreetMap in many areas.
- Available at: github.com/microsoft/USBuildingFootprints

### FEMA USA Structures
A national building footprint dataset maintained by FEMA with attribute data including occupancy type. Useful for community-scale analysis.

---

## A Note on Data Quality

Finding a dataset is not the same as understanding it. Before using any dataset, ask:

- Who collected it, and how?
- What are the known limitations or gaps?
- Has it been used in peer-reviewed research? (If so, cite those papers and read how they handled the limitations.)
- Is it the most current version available?

When in doubt, ask Rebecca before building analysis on top of a dataset you are not confident in.
