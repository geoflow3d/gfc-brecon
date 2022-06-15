# Building reconstruction flowcharts for Geoflow
This repository contains the flowcharts to get started with building reconstruction with the Geoflow software.

## How to do it
From the root of this repository run

```
geof single/reconstruct.json \
  --input_footprint=test-data/wippolder.gpkg \
  --input_pointcloud=test-data/wippolder.las \
  --config single/config.toml
```
