# Methodology

This document describes the hydrological methodology used to derive
catchment parameters for HEC-HMS from a Digital Elevation Model (DEM).

## 1. DEM Preprocessing
Raw DEMs often contain sinks and depressions that disrupt hydrological
flow modeling. Sink filling is applied to ensure continuous downhill flow.

## 2. Flow Direction
Flow direction is computed using the D8 algorithm, where each raster cell
routes flow to the steepest downslope neighbor.

## 3. Flow Accumulation
Flow accumulation represents the number of upstream cells contributing
flow to each cell and is used to identify drainage paths.

## 4. Stream Extraction
A flow accumulation threshold is applied to extract stream networks.
Higher thresholds produce major streams, while lower thresholds include
minor tributaries.

## 5. Basin Delineation
Watersheds and sub-basins are delineated using flow direction and stream
outlets.

## 6. Hydrological Post-Processing
Post-processing steps include stream cleaning, basin refinement, and
geometric calculations.

## 7. HEC-HMS Parameter Extraction
Derived parameters include:
- Basin area
- Basin slope
- Longest flow path
- Stream length
- Reach slope
- Time of concentration (where applicable)

These parameters are exported in tabular format for direct use in
HEC-HMS.
