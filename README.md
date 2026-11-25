# WaTEM/SEDEM Output Analysis

A small Python project that turns a raw WaTEM/SEDEM text output into a clear
summary of catchment sediment results.

## Data
`data/Total sediment.txt`: output of one WaTEM/SEDEM run (values in kg).

## What I did
- Parsed the "name: value (unit)" lines into a Python dictionary
- Calculated the deposition ratio and the export ratio
- Summarised the results in a pandas table

## Results
| Parameter | Value |
|---|---|
| Total erosion | 22,656,029 kg |
| Total deposition | 18,383,995 kg |
| Deposition ratio | 81.1 % |
| Export ratio | 9.1 % |

About 81 % of the eroded soil is deposited again inside the catchment;
only about 9 % leaves it. (The model reports erosion as a negative number;
shown here as positive for readability.)

## Run it
Open `sediment_analysis.ipynb` in Jupyter from the project folder.

Tools: Python, pandas, Matplotlib
