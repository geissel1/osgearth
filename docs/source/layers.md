# osgEarth Layers

These are the public layer types native to osgEarth.

## Imagery

| Earth File                                                   | API class                   | Description                                                  |
| ------------------------------------------------------------ | --------------------------- | ------------------------------------------------------------ |
| [ArcGISServerImage](layers/ArcGISServerImageLayer.html)      | ArcGISServerImageLayer      | Connects to an ESRI ArcGIS Server instance                   |
| [ArcGISTilePackageImage](layers/ArcGISTilePackageImageLayer.html) | ArcGISTilePackageImageLayer | Reads an ESRI ArcGIS Tile Package                            |
| [BingImage](layers/BingImageLayer.html)                      | BingImageLayer              | Connects to Microsoft Bing service. License key required     |
| [CesiumIonImage](layers/CesiumIonImageLayer.html)            | CesiumIonImageLayer         | Connects to a Cesium Ion server instance. Key required       |
| [CompositeImage](layers/CompositeImageLayer.html)            | CompositeImageLayer         | Combines multiple image layers into a single map layer       |
| [ContourMap](layers/ContourMapLayer.html)                    | ContourMapLayer             | Renders a colored representation of the elevation data in the map |
| [GDALImage](layers/GDALImageLayer.html)                      | GDALImageLayer              | Loads any imagery format supported by the GDAL library, including GeoTIFF |
| [GDALDEM](layers/GDALDEMLayer.html)                          | GDALDEMLayer                | Renders various rasterized shaded elevation maps             |
| [MBTilesImage](layers/MBTilesImageLayer.html)                | MBTilesImageLayer           | Reads imagery tiles from an MBTiles (MapBox Tiles) database file |
| [TMSImage](layers/TMSImageLayer.html)                        | TMSImageLayer               | Connects to a TMS (TileMapService) data source               |
| [WMSImage](layers/WMSImageLayer.html)                          | WMSImageLayer               | Connects to an OGC Web Map Service server                    |
| [XYZImage](layers/XYZImageLayer.html)                        | XYZImageLayer               | Reads imagery tiles in standard XYZ format (no metadata)     |



## Terrain Elevation

| Earth File         | API Class               | Description                                                  |
| ------------------ | ----------------------- | ------------------------------------------------------------ |
| FlattenedElevation | FlatteningLayer         | Alters elevation data to flatten it to a specific elevation value; useful for flattening a region where you intend to place a site model |
| BingElevation      | BingElevationLayer      | Connects to Microsoft Bing elevation service. License key required |
| CompositeElevation | CompositeElevationLayer | Combines multiple elevation layers into a single map layer   |
| GDALElevation      | GDALElevationLayer      | Loads any elevation format supported by the GDAL library, including GeoTIFF |
| MBTilesElevation   | MBTilesElevationLayer   | Reads elevation data stored in an MBTiles (MapBox Tiles) database file |
| TMSElevation       | TMSElevationLayer       | Connects to an OSGeo Tile Map Service data source (locally or networked) |
| XYZElevation       | XYZElevationLayer       | Reads elevation tiles in standard XYZ format (no metadata)   |



## Vector Features

| Earth File        | API Class              | Description                                                  |
| ----------------- | ---------------------- | ------------------------------------------------------------ |
| FeatureImage      | FeatureImageLayer      | Rasterizes vector data into an image layer                   |
| FeatureModel      | FeatureModelLayer      | Renders vector data as *OpenSceneGraph* geometry             |
| TiledFeatureModel | TiledFeatureModelLayer | Like a `FeatureModel` layer, but optimized for pre-tiled vector datasets |



## Miscellaneous

| Earth File        | API Class              | Description                                                  |
| ----------------- | ---------------------- | ------------------------------------------------------------ |
| Annotations       | AnnotationLayer        | Holds a collection of annotation elements (like text labels, place nodes, or features) |
| Debug             | DebugImageLayer        | Renders metadata about each rendered map tile                |
| GeodeticGraticule | GeodeticGraticuleLayer | Display a simple latitude/longitude graticule                |
| MGRSGraticule     | MGRSGraticuleLayer     | Displays a simple MGRS graticule with labels                 |
| Model             | ModelLayer             | Loads and displays an external 3D model at a map location    |
| Ocean             | SimpleOceanLayer       | Renders a very simple ocean surface (requires the map to have bathymetry data) |
| Sky               | SimpleSkyLayer         | Renders a sky model with realistic lighting and shading      |
| TerrainConstraint | TerrainConstraintLayer | Alters the triangulation of the terrain skin to incorporate vector data; e.g., to represent ridgelines, coastlines, or to cut out an area where a custom terrain model will go |
| ThreeDTiles       | ThreeDTilesLayer       | Displays a 3D-Tiles dataset                                  |
| UTMGraticule      | UTMGraticuleLayer      | Displays a simple UTM graticule                              |
| Video             | VideoLayer             | Renders various video formats to a layer (using FFMPEG)      |
| Viewpoints        | ViewpointsLayer        | Pre-set viewpoints that a viewer application can display for the user |
| Wind              | WindLayer              | Incorporates a wind model (needs other layers that can use the data) |



## Feature Sources

| Earth File  | API Class        | Description                                                  |
| ----------- | ---------------- | ------------------------------------------------------------ |
| MVTFeatures | MVTFeatureSource | Mapnik Vector Tiles specification                            |
| OGRFeatures | OGRFeatureSource | Uses a GDAL/OGR vector driver to read feature data. This is the most common feature source for reading local data (e.g., ESRI Shapefile) |
| TFSFeatures | TFSFeatureSource | Reads vector features from a server according to the Tiled Feature Service specification (osgEarth proprietary) |
| WFSFeatures | WFSFeatureSource | OGC Web Feature Service specification (limited implementation) |
| XYZFeatures | XZYFeatureSource | Generic specification for reading tiled vector data from a server |