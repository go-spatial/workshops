# Slides are available at:

http://bit.ly/foss4g2018tegola

## Package contents.
```
├┬─binary
│├┬─mac
││├──tegola
││└──fresco
│├┬─windows
││├──tegola.exe
││└──fresco.exe
│└┬─linux
│ ├──tegola
│ └──fresco
├┬─config               # compleated config files.
│├──config_5.toml
│├──config_4.toml
│├──config_3.toml
│├──config_2.toml
│└──config_1.toml
├┬─raw 			# data files.
│├──ne_110m_populated_places_simple.zip
│├──ne_110m_land.zip
│├──ne_10m_time_zones.zip
│├──ne_10m_parks_and_protected_lands.zip
│├──ne_10m_land.zip
│└──belize-latest.osm.pbf
├──style.json           # initial style file
├──populated.gpkg       # populated city db
├──naturalearth.gpkg    # land polygon db
├──config.toml          # initial config files.
└──README.md
```

How to create the gpkg pacakge from the shp file using ogr2ogr.

```
OGR_ENABLE_PARTIAL_REPROJECTION=true ogr2ogr -overwrite -nlt PROMOTE_TO_MULTI -f GPKG naturalearth.gpkg ne_10m_land/ne_10m_land.shp
```
