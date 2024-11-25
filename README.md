# District Accessibility Analysis of Tram Stops in Amsterdam

## Objective
The aim of this project is to analyze the accessibility of tram stops in Amsterdam by calculating the proportion of district areas (from the "Wijken" layer) that fall within a 500-meter walking distance of a tram stop. This analysis identifies districts underserved by public transport, providing insights for urban planning and transport optimization.

## Data Used

- Tram Stop Locations:
Source: [Amsterdam Open Geodata Portal](https://maps.amsterdam.nl/open_geodata/geojson_lnglat.php?KAARTLAAG=TRAMMETRO_PUNTEN_2024&THEMA=trammetro)
Description: Point data representing the locations of tram stops in Amsterdam.

- District Boundaries ("Wijken"):
Source: Amsterdam BAG GeoPackage
Description: Polygon data representing the administrative districts (Wijken) of Amsterdam.

## Tools and Libraries

Programming Language: Python

Key Libraries:

GeoPandas: For spatial data manipulation and overlay operations.
Matplotlib: For creating static maps.
Folium: For interactive visualizations.

## Approach

Step 1: Loading the Data: I loaded tram stop location data from the GeoJSON file and extracted the district boundaries from the GeoPackage layer named "Wijken".

Step 2: Buffer Analysis: I created 500-meter buffers around tram stops to represent accessible walking areas.

Step 3: Dissolving Overlapping Buffers: I merged overlapping buffers to prevent double-counting accessible areas.

Step 4: Spatial Intersection: I intersected the tram stop buffers with district boundaries to calculate the proportion of each district covered.

Step 5: Visualization: I generated a choropleth map showing district-level tram stop accessibility.
