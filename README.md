# LEDs Payload PCB

LED array PCB for the optical downlink payload of the TEIDESAT-1 CubeSat.
The board emits modulated light pulses towards ground stations.

## Status

**v0.3** — layout complete, ready for manufacturing.
This version is intended to validate the predictions of the satellite's
transient thermal study.

## Design summary

- **LEDs:** 260 LEDs in 65 groups of 4 in series (12 V per group).
  Group placement was generated with an automated packing script,
  using line, L, Z, T and square group shapes.
- **Stackup (4 layers, top to bottom):** driver connectors / GND / 12V / LEDs.
- **Power distribution:** copper zones instead of tracks.
- **Vias:** through vias (blind vias were not available in the manufacturing process).
- **Connectors:** 5-pin (4-pin parts were out of stock). Required current capacity: 23 A.
- **Central opening:** leaves room for the optical board mounted behind.
- The LED driver is a separate PCB; it connects to this board through global connectors.

## Repository structure

- `hardware/` — KiCad project (schematic, PCB, project file and custom symbol/footprint/3D libraries).

Open with **KiCad 10.0.5** or newer.

## Open items / future versions

- Thermal: no copper changes for heat dissipation in v0.3. The board is planned
  to be mounted on an aluminium plate; check the risk of shorts through the through vias.
