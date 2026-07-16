# Comparative Analysis

The same PicoRV32 RISC-V processor was implemented using both OpenLane (Sky130) and Cadence (GPDK90).

## Routing Stage Comparison

| Parameter | OpenLane (Sky130) | Cadence (GPDK90) |
|-----------|------------------:|-----------------:|
| Total Power | 2.25 × 10⁻³ W | 1.11 × 10⁻³ W |
| Area | 123315 µm² | 85116 µm² |
| Setup Slack | 92.31 ns | 84.711 ns |
| Hold Slack | 0.39 ns | 0.01 ns |

## Key Findings

- Cadence achieved approximately **50.7% lower total power**.
- Cadence occupied approximately **31% less silicon area**.
- Both implementations achieved positive setup and hold timing.
- OpenLane required no additional hold-time optimization.
- Cadence initially exhibited hold violations that were resolved after optimization.

## Conclusion

Both flows successfully completed RTL-to-GDSII implementation of PicoRV32. Cadence produced a smaller and lower-power implementation, while OpenLane demonstrated a fully open-source implementation flow capable of achieving timing closure and successful GDSII generation.

# Observations and Discussion

## OpenLane (Sky130)

- Successfully completed synthesis, floorplanning, placement, CTS, routing, and signoff.
- Final routing power measured 2.25 × 10⁻³ W.
- Final routed area measured 123315 µm².
- Positive setup slack of 92.31 ns.
- Positive hold slack of 0.39 ns.
- Successfully generated manufacturable GDSII.

## Cadence (GPDK90)

- Successfully synthesized using Cadence Genus.
- Successfully completed place-and-route using Innovus.
- Final routing power measured 1.11 × 10⁻³ W.
- Final routed area measured 85116 µm².
- Final setup slack of 84.711 ns.
- Final hold slack of 0.01 ns after optimization.
- Successfully generated final GDSII.

## Overall Discussion

The commercial Cadence implementation achieved lower power consumption and reduced silicon area due to the 90 nm technology node and advanced optimization capabilities. The OpenLane implementation demonstrated that a complete open-source RTL-to-GDSII flow can successfully implement a complex RISC-V processor while achieving positive timing closure and generating a manufacturable GDSII layout.
