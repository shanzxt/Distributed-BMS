# Sensor Selection Report

**Owner:** _(assign)_  **Status:** Draft  **Last updated:** 2026-10-26

Purpose: identify the sensors and measurement circuits needed for cell monitoring, SOC estimation and fault detection in the distributed BMS.

## 1. What must be measured

| Parameter | Why it is needed | Used for |
|---|---|---|
| Cell voltage (per cell) | Over/under-voltage protection, imbalance detection, OCV-based SOC correction | SOC, faults, balancing |
| Cell/module temperature | Over-temperature protection, temperature-dependent model parameters | SOC, faults |
| Pack current | Coulomb counting, over-current protection, internal resistance estimation | SOC, faults |
| Pack voltage (optional) | Cross-check against sum of cell voltages (sensor fault detection) | Faults |

## 2. Measurement principles

| Parameter | Sensor / method | Conversion trick |
|---|---|---|
| Cell voltage | Battery monitor IC (AFE) with internal mux, level shift and ADC; or external ADC + mux | Taps at each cell boundary; AFE handles the high common-mode voltage |
| Temperature | NTC thermistor (e.g. 10 kΩ, B≈3950) | Voltage divider to ADC, then lookup table or Steinhart-Hart |
| Current | Shunt resistor + amplifier, or Hall-effect sensor | Shunt: tiny voltage amplified. Hall: magnetic field, isolated, no I²R loss |

Key reasoning to document:
- An MCU ADC (about 3.3 V) cannot read the top cell of a series stack directly, which is why AFEs exist.
- Shunt trade-off: bigger resistance gives more signal but more heat (P = I²R). Example: 1 mΩ at 100 A dissipates about 10 W.
- Current accuracy drives SOC accuracy: Coulomb counting integrates current, so a constant offset becomes a growing error.

## 3. Candidate parts (to be filled in)

| Function | Candidate | Key specs (accuracy, range, resolution) | Cost (INR) | Source / datasheet link | Decision |
|---|---|---|---|---|---|
| Cell monitor / AFE | _TBD_ | | | | |
| MCU (slave) | _TBD_ | | | | |
| MCU (master) | _TBD_ | | | | |
| Thermistor | _TBD_ | | | | |
| Current sensor | _TBD_ | | | | |
| CAN transceiver | _TBD_ | | | | |

Reference architecture material: TI white paper SLYY197 (wired vs wireless BMS) and TI reference design TIDUF92. These are automotive-grade parts and likely too expensive; use them to learn the architecture, then choose a student-budget equivalent.

## 4. Requirements to fix before choosing parts

- [ ] Cell chemistry (NMC or LFP) and cell format (18650 recommended for a student build)
- [ ] Series count (e.g. 4S or 8S) and number of slave modules
- [ ] Maximum charge/discharge current
- [ ] Target voltage accuracy (mV) and SOC accuracy (%)
- [ ] Sampling rate
- [ ] Budget (confirm with KPIT guide)
- [ ] Safety rules for handling lithium cells (confirm with KPIT guide)

## 5. Open questions

- Does the lab already have an AFE evaluation board or sensors we can reuse?
- Do we need isolated current sensing, or is a shunt acceptable at our pack voltage?
