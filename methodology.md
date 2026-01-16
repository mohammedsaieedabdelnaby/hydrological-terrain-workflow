This document describes the hydrological methodology used to derive
catchment parameters for HEC-HMS from a Digital Elevation Model (DEM).

## 1. DEM Preprocessing
Raw DEMs often contain sinks and depressions that disrupt hydrological
flow modeling. Sink filling is applied to ensure continuous downhill flow.


<img width="942" height="617" alt="image" src="https://github.com/user-attachments/assets/5763efe4-a7ed-40c6-a69d-8ac3c62a3ae6" />

## 2. Flow Direction
Flow direction is computed using the D8 algorithm, where each raster cell
routes flow to the steepest downslope neighbor.

<img width="897" height="563" alt="image" src="https://github.com/user-attachments/assets/16f6587e-e7c4-412a-9e03-5c733d489553" />


## 3. Flow Accumulation
Flow accumulation represents the number of upstream cells contributing
flow to each cell and is used to identify drainage paths.

<img width="900" height="562" alt="image" src="https://github.com/user-attachments/assets/b5c94669-9890-4f1f-b178-49cc6a5af090" />


## 4. Stream Extraction
A flow accumulation threshold is applied to extract stream networks.
Higher thresholds produce major streams, while lower thresholds include
minor tributaries.

<img width="848" height="612" alt="image" src="https://github.com/user-attachments/assets/7e2442d7-b200-445f-865a-8894ed877d99" />


## 5. Basin Delineation
Watersheds and sub-basins are delineated using flow direction and stream
outlets.

<img width="831" height="617" alt="image" src="https://github.com/user-attachments/assets/90754025-49a3-47e3-9110-ccd571124bf7" />


## 6. Hydrological Post-Processing
Post-processing steps include stream cleaning, basin refinement, and
geometric calculations.

<img width="792" height="483" alt="image" src="https://github.com/user-attachments/assets/63d6d73b-f938-41fc-aca0-ce8b303fff0d" />


## 7. HEC-HMS Parameter Extraction
Derived parameters include:
- Basin area
- Basin slope
- Longest flow path
- Stream length
- Reach slope
- Time of concentration (where applicable) Using kirpich Equation $t_c = K \cdot L^{0.77} \cdot S^{-0.385}$


These parameters are exported in tabular format for direct use in
HEC-HMS.


<img width="1502" height="73" alt="image" src="https://github.com/user-attachments/assets/08aa5b6b-8fc2-4b92-90e0-d0f92c27a22d" />



