# Dataset Assessment

**Owner:** _(assign)_  **Status:** Draft  **Last updated:** 2026-10-26

Goal: find public datasets with voltage, current, temperature, SOC and fault-related measurements, and decide whether they are enough or whether we must collect our own data in the lab.

## Candidate datasets (from memory; confirm every detail at the source)

| Dataset | Source | Parameters | Operating conditions | Format | Good for | Caveats | Verified |
|---|---|---|---|---|---|---|---|
| NASA PCoE Li-ion battery aging | NASA Prognostics Center of Excellence repository | V, I, T, capacity over cycles | Room temp and others, charge/discharge cycles | MATLAB .mat | SOH/aging | Limited SOC ground truth, few cells | No |
| CALCE battery data | University of Maryland CALCE | V, I, T, capacity | Various cells and profiles | Excel/MATLAB | SOC, aging | Check cell type and profiles | No |
| Oxford battery degradation | University of Oxford | V, T, aging cycles | Drive-cycle-like profiles | MATLAB | Aging | Small cells | No |
| Panasonic 18650PF drive cycles | Mendeley Data (McMaster) | V, I, T, SOC | Multiple temperatures, drive cycles | CSV/MATLAB | SOC estimation | Single cell, lab conditions | No |
| Real-world EV fault dataset (paper 7) | Nature Commun. 14, 5940; figshare link in paper | Charging snippets from many EVs | Real EVs | See source | Fault/anomaly detection | Pack-level, not per-cell distributed | No |

## Assessment criteria (fill for each dataset)

- [ ] Has V, I and T at a usable sampling rate
- [ ] Has SOC ground truth, or enough information to compute it
- [ ] Cell chemistry close to ours (NMC vs LFP)
- [ ] Includes fault or abnormal behaviour
- [ ] Multi-cell or pack-level data (needed for the distributed angle)
- [ ] License allows our use (research, publication)
- [ ] Format convenient (CSV, .mat)

## Key question

Most public data is single-cell. A distributed multi-cell BMS needs **per-cell data across a series string, including a failed sensor or a dropped node**. Public data likely will not cover this, which suggests we must also collect our own data from a small pack and inject faults (simulated sensor dropout, thermal anomaly). Confirm feasibility with the KPIT guide.

## Decision log

| Date | Decision | Reason |
|---|---|---|
| | | |
