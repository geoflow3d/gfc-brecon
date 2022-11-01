# Building reconstruction flowcharts for Geoflow
This folder contains the flowcharts to get started with building reconstruction with the Geoflow software in stream reconstruction (reconstruct with one process per building for large numbers of buildings).

## How to do it
Download test data from `https://data.3dgi.xyz/geoflow-test-data/wippolder.zip` and unzip into `test-data` directory, eg on unix commandline:
```
wget https://data.3dgi.xyz/geoflow-test-data/wippolder.zip
unzip wippolder.zip -b test-data
```

Then run:
```
geof crop.json \
  --INPUT_FOOTPRINT_SOURCE=test-data/wippolder.gpkg \
  --INPUT_LAS_FILES=test-data/wippolder.las \
  --OUTPUT_DIR=output \
  --DATASET_TITLE=wippolder \
  --TILE_ID=1 \
```
This will prepare all the inputs for every building in the output folder.

Then:
```
find output -path "output/wippolder/1/*/config.toml" | parallel geof reconstruct.json --config {1}
```
To run the reconstruction in parallel for all the buildings.