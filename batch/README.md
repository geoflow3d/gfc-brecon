# Building reconstruction flowcharts for Geoflow
This folder contains the flowcharts to get started with building reconstruction with the Geoflow software in batch reconstruction (reconstruct all buildings in input footprint file).

## How to do it
Download test data from `https://data.3dgi.xyz/geoflow-test-data/wippolder.zip` and unzip into `test-data` directory, eg on unix commandline:
```
wget https://data.3dgi.xyz/geoflow-test-data/wippolder.zip
unzip wippolder.zip -b test-data
```

Then run:
```
geof reconstruct.json \
  --input_footprint=test-data/wippolder.gpkg \
  --input_pointcloud=test-data/wippolder.las \
```
