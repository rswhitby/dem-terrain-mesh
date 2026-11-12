# DEM to Terrain Mesh

A browser tool that converts GeoTIFF elevation tiles (DEMs) into a terrain mesh for Rhino.

**Use it:** open the GitHub Pages link for this repository.

1. Load one or more adjacent GeoTIFF tiles in a projected coordinate system (for example UTM).
2. Drag a box on the shaded map to choose the area.
3. Set units, resolution, origin, vertical exaggeration and an optional solid base.
4. Preview in 3D and download a .zip with the mesh (.obj) and an info file with the origin coordinates.

Files are processed in the browser and are not uploaded anywhere.

## Importing into Rhino
- Import the .obj. Leave "Map OBJ Y to Rhino Z" unchecked; the file is already Z-up.
- Set the Rhino model units to the output units chosen in the tool.

## Data sources
- New York State: Discover GIS Data NY (gis.ny.gov), DEM Results > Null tab > 1 Meter DEM Index (NYS).
- United States: USGS National Map Downloader, 1 meter DEM.

A DEM shows bare ground only. Trees and buildings are removed and water surfaces are flattened.

## Libraries
geotiff.js, three.js, JSZip (loaded from public CDNs).
