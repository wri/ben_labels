### Big Earth Net: meta data

[Big Earth Net](http://bigearth.net/) has labeled close to 600,000 Sentinel-2 tiles. This will prove to be extremely useful for a number of projects.

The data is organized such that there is a directory per tile containing a tif file for each individual band and a json file containing the labels along with other meta data. The directory level json files are sufficient, but are not useful if one is looking to balance or select data based on tiles. Additionally [Big Earth Net](http://bigearth.net/) contains files with the tile_ids containing clouds/shadows, and seasonal snow.

Here we collect all the labels, along with its cloud/snow state, into a single csv.  Additionally we add a number of other files which might be useful to anyone working with Big Earth Net.

---

#### FILES:

1. labels_clouds_snow-[1](https://github.com/wri/ben_labels/blob/master/labels_clouds_snow-1-v1.0.csv)/[2](https://github.com/wri/ben_labels/blob/master/labels_clouds_snow-1-v1.0.csv)-v1.0: CSVs containing tile_id,cloud/shadow,seasonal-snow and a boolean column for each BigEarthNet Label. 
2. [labels_counts](https://github.com/wri/ben_labels/blob/master/labels_counts.csv): CSV containing BigEarthNet Labels and tile-count for each
3. [sentinel2_bands](https://github.com/wri/ben_labels/blob/master/sentinel2_bands.csv): CSV containing relevant data for each Sentinel-2 band
4. [patches_with_cloud_and_shadow](https://github.com/wri/ben_labels/blob/master/patches_with_cloud_and_shadow.csv): BigEarthNet's cloud/shadow CSV (no changes)
5. [patches_with_seasonal_snow](https://github.com/wri/ben_labels/blob/master/patches_with_seasonal_snow.csv): BigEarthNet's seasonal-snow CSV (no changes)

---

#### NOTES:

Notes: 

* (1) has been broken into two files due to github's file size restrictions. The reduced files size is also useful if one doesn't need all 600,000 images.  
* (4) and (5) files can be downloaded directly from [Big Earth Net](http://bigearth.net/).


```
# Big Earth Net Labels (in descending order of occurrence)
LABELS=[
    'Mixed forest',
    'Coniferous forest',
    'Non-irrigated arable land',
    'Transitional woodland/shrub',
    'Broad-leaved forest',
    'Land principally occupied by agriculture, with significant areas of natural vegetation',
    'Complex cultivation patterns',
    'Pastures',
    'Water bodies',
    'Sea and ocean',
    'Discontinuous urban fabric',
    'Agro-forestry areas',
    'Peatbogs',
    'Permanently irrigated land',
    'Industrial or commercial units',
    'Natural grassland',
    'Olive groves',
    'Sclerophyllous vegetation',
    'Continuous urban fabric',
    'Water courses',
    'Vineyards',
    'Annual crops associated with permanent crops',
    'Inland marshes',
    'Moors and heathland',
    'Sport and leisure facilities',
    'Fruit trees and berry plantations',
    'Mineral extraction sites',
    'Rice fields',
    'Road and rail networks and associated land',
    'Bare rock',
    'Green urban areas',
    'Beaches, dunes, sands',
    'Sparsely vegetated areas',
    'Salt marshes',
    'Coastal lagoons',
    'Construction sites',
    'Estuaries',
    'Intertidal flats',
    'Airports',
    'Dump sites',
    'Port areas',
    'Salines',
    'Burnt areas']
```