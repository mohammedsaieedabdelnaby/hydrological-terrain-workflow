# hydrological-terrain-workflow
  # DEM to HEC-HMS Catchment Parameters

End-to-end workflow to extract HEC-HMS catchment parameters from
Digital Elevation Models (DEM) using hydrological terrain analysis
and post-processing.

## Overview
This project demonstrates how raw DEM data can be processed to derive
hydrological features and catchment parameters required for
HEC-HMS hydrological modeling.

The workflow follows standard hydrological preprocessing and
post-processing practices used in GIS and hydrology.

## Workflow
1. DEM preprocessing (sink filling)
2. Flow direction calculation (D8 method)
3. Flow accumulation analysis
4. Stream network extraction
5. Watershed / basin delineation
6. Hydrological post-processing
7. Extraction of HEC-HMS catchment parameters

## Outputs
- Delineated basins
- Stream network
- Catchment parameters table compatible with HEC-HMS

## Repository Structure
- `notebooks/` – Jupyter notebooks containing the workflow
- `data/` – Input DEM data
- `outputs/` – Generated hydrological outputs
- `docs/` – Methodology and documentation

## Applications
- HEC-HMS basin modeling
- Flood modeling
- Watershed analysis
- Hydrological studies

## License
MIT License
