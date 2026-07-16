# Cadence Reports (GPDK90)

This directory contains implementation reports generated using Cadence Genus and Innovus for the PicoRV32 RISC-V processor.

## Design Flow

- RTL Synthesis (Genus)
- Physical Design (Innovus)
- Clock Tree Synthesis
- Routing
- GDSII Generation

## Final Implementation Results

### Power

| Stage | Total Power (W) |
|--------|-----------------:|
| Synthesis | 1.09 × 10⁻³ |
| Placement | 1.09 × 10⁻³ |
| CTS | 1.11 × 10⁻³ |
| Routing | 1.11 × 10⁻³ |

### Area

| Stage | Area (µm²) |
|--------|-----------:|
| Synthesis | 85108.107 |
| Placement | 85108.107 |
| CTS | 85116 |
| Routing | 85116 |

### Timing

| Stage | Setup Slack (ns) | Hold Slack (ns) |
|--------|-----------------:|----------------:|
| Synthesis | 85.133 | 0.02 |
| Placement | 84.924 | 0.01 |
| CTS | 84.700 | 0.01 |
| Routing | 84.711 | 0.01 |

## Summary

- Successful synthesis using Cadence Genus
- Successful physical implementation using Cadence Innovus
- Final GDSII generated successfully
- Timing optimized to achieve positive hold slack
