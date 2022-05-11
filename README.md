# Building reconstruction flowcharts for Geoflow
This repository contains the flowcharts to get started with building reconstruction with the Geoflow software.

## How to do it
From the root of this repositoty run

```
geof crop.json
find reconstruct/crop/*/config.toml | parallel geof reconstruct.json --config {1} --log {1}.loggfc-brecon
