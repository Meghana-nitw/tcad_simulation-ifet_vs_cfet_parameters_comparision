# tcad_simulation-ifet_vs_cfet_parameters_comparision
# Comparative Analysis of iFET and CFET with Negative Capacitance

## Project Overview

This project presents a comparative study of **iFET and CFET transistor architectures**, with and without Negative Capacitance (NC), using TCAD simulations.

The objective is to investigate their electrical characteristics, extract important device parameters, and evaluate their performance in terms of drive current, leakage current, switching speed, and linearity.

Four device configurations are analyzed:

1. iFET
2. iFET with Negative Capacitance (iFET + NC)
3. CFET
4. CFET with Negative Capacitance (CFET + NC)

## Objectives

- Compare the electrical characteristics of iFET and CFET structures.
- Analyze the impact of Negative Capacitance on transistor performance.
- Generate and study ID–VGS, ID–VDS, and C–V characteristics.
- Extract important parameters such as ION, IOFF, VTH, SS, DIBL, gm, gds, and Cgg.
- Evaluate intrinsic delay and linearity parameters.
- Identify performance trade-offs among the four device configurations.

## Simulation and Analysis

The project follows a simulation and parameter-extraction workflow.

### 1. ID–VGS Characteristics

- Simulated drain current against gate-to-source voltage.
- Studied both linear-scale and logarithmic-scale characteristics.
- Used VDS = 0.7 V and swept VGS from 0 V to 0.8 V.
- Compared ON-state and OFF-state current behavior.

### 2. ID–VDS Characteristics

- Analyzed drain current against drain-to-source voltage.
- Studied the linear and saturation regions.
- Compared the output characteristics of all four configurations.

### 3. C–V Characteristics

- Analyzed gate capacitance using AC small-signal simulation.
- Extracted gate capacitance (Cgg).
- Investigated the relationship between gate capacitance and device switching performance.

### 4. Parameter Extraction

The following device parameters were evaluated:

- ON-state current (ION)
- OFF-state current (IOFF)
- Threshold voltage (VTH)
- Subthreshold swing (SS)
- Drain-induced barrier lowering (DIBL)
- Transconductance (gm)
- Output conductance (gds)
- Gate capacitance (Cgg)

### 5. Performance Evaluation

Python-based post-processing was used to evaluate:

- Intrinsic device delay
- Second-order voltage intercept point (VIP2)
- Third-order input intercept point (IIP3)
- 1-dB compression point

## Tools and Technologies

- **Synopsys Sentaurus TCAD:** Device simulation and electrical characteristic analysis.
- **Python:** Numerical calculations and performance parameter extraction.
- **Origin-style plotting:** Graph visualization and comparative analysis.

## Results and Comparison

The following values are from the project's extracted results.

### ON-State Current (ION)

| Device | ION (µA) |
|---|---:|
| iFET | 61.3 |
| iFET + NC | 64.4 |
| CFET | 159.8 |
| CFET + NC | 208.0 |

### ION/IOFF Ratio and Threshold Voltage

| Device | ION/IOFF | VTH (V) |
|---|---:|---:|
| iFET | 2.02 × 10⁷ | 0.245 |
| iFET + NC | 3.11 × 10⁷ | 0.259 |
| CFET | 5.65 × 10⁷ | 0.314 |
| CFET + NC | 4.32 × 10⁸ | 0.344 |

### Peak Transconductance

| Device | gm (mS) |
|---|---:|
| iFET | 0.347 |
| iFET + NC | 0.370 |
| CFET | 3.23 |
| CFET + NC | 3.92 |

### Intrinsic Delay

| Device | Delay (ps) |
|---|---:|
| iFET | 0.92 |
| iFET + NC | 0.87 |
| CFET | 1.06 |
| CFET + NC | 0.77 |

## Key Observations

- CFET configurations demonstrate higher ON-state current compared with iFET configurations.
- CFET with Negative Capacitance achieves the highest reported ON-state current and ION/IOFF ratio.
- Negative Capacitance improves the reported intrinsic delay for both device architectures.
- CFET with Negative Capacitance exhibits the lowest reported intrinsic delay of 0.77 ps at VGS = 0.8 V.
- iFET configurations demonstrate better reported linearity performance at higher gate voltages (VGS > 0.5 V).

## Conclusion

The comparative analysis highlights the performance differences between iFET and CFET architectures and investigates the influence of Negative Capacitance on their electrical characteristics.

Among the four configurations, CFET with Negative Capacitance demonstrates the strongest reported drive current and lowest intrinsic delay, while iFET configurations show advantages in the evaluated linearity characteristics.

The study provides a comparative understanding of transistor-level performance trade-offs for future high-performance and low-power semiconductor devices.

## Author

**Meghana Poduri**  
B.Tech – Electronics and Communication Engineering (VLSI-DT)  
National Institute of Technology Warangal


## Note on Results

The reported SS and DIBL values require further validation. The extracted SS values for some configurations are below the conventional 60 mV/dec thermal limit, and the low-drain-bias threshold-voltage values used in DIBL extraction need to be checked. These parameters should be re-extracted before treating them as final validated results.
