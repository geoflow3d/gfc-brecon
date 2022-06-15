# Building reconstruction flowcharts for Geoflow
This repository contains the flowcharts to get started with building reconstruction with the Geoflow software.

## How to do it
Download some test data from `https://data.3dgi.xyz/geoflow-test-data`.
The following instruction works if you have placed the test data sets into a `test-data` directory in this repository.

Then from the root of this repository run:

```
geof single/reconstruct.json \
  --input_footprint=test-data/wippolder.gpkg \
  --input_pointcloud=test-data/wippolder.las \
  --config single/config.toml
```
