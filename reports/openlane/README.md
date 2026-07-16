# OpenLane Reports (Sky130)

This directory contains implementation reports generated using the OpenLane RTL-to-GDSII flow for the PicoRV32 RISC-V processor.

## Design Flow

- RTL Synthesis (Yosys)
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Routing
- GDSII Generation

## Final Implementation Results

### Power

| Stage | Total Power (W) |
|--------|-----------------:|
| Synthesis | 1.74 × 10⁻³ |
| Placement | 2.04 × 10⁻³ |
| CTS | 2.65 × 10⁻³ |
| Routing | 2.25 × 10⁻³ |

### Area

| Stage | Area (µm²) |
|--------|-----------:|
| Synthesis | 111275.472 |
| Placement | 116706 |
| CTS | 122691 |
| Routing | 123315 |

### Timing

| Stage | Setup Slack (ns) | Hold Slack (ns) |
|--------|-----------------:|----------------:|
| Synthesis | 91.52 | 0.43 |
| Placement | 91.74 | 0.44 |
| CTS | 91.76 | 0.46 |
| Routing | 92.31 | 0.39 |

## Summary

- Successful RTL-to-GDSII implementation
- Positive setup and hold slack throughout the flow
- Final GDSII generated successfully using Sky130 PDK
