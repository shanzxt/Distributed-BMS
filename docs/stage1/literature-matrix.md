# Literature Review Matrix

**Owner:** _(assign)_  **Status:** Draft  **Last updated:** 2026-10-26

## How to use this file

For every paper record the six items below. **Do not trust any pre-filled summary until the "Verified" column says Yes.** Verification means: you opened the DOI or link yourself, and the title, venue, year and the claims you recorded match the paper.

| Column | Meaning |
|---|---|
| Problem | Problem addressed |
| Inputs / dataset | Sensor inputs and dataset used |
| Method | Algorithm or methodology |
| Claimed contribution | Novel contribution claimed by the authors |
| Limitations | Limitations and future work |
| Relevance | Relevance to our distributed BMS and potential research gap |
| Verified | Yes / No (who, date) |

Suggested reading order (from the shared list): start with papers 1, 4, 7 and 9, then the rest.

## Matrix (from the shared reading list; pre-filled fields are summaries, not verified)

| # | Paper | Venue / year | Link | Problem | Inputs / dataset | Method | Claimed contribution | Limitations | Relevance | Verified |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Distributed Intelligent Battery Management System Using a Real-World Cloud Computing System | Sensors 23(7), 3417, 2023 | https://pmc.ncbi.nlm.nih.gov/articles/PMC10098843/ | Coordinating monitors, controllers and charging in a real BMS | | | Decentralized but synchronized system with networked monitors and cloud | | Local nodes vs master split | No |
| 2 | Recent Developments and Challenges in SOC Estimation Techniques for EV Batteries: A Review | J. Energy Storage, 2024, DOI 10.1016/j.est.2024.113623 | https://doi.org/10.1016/j.est.2024.113623 | SOC estimation under varying load/temperature/condition | | | Reviews conventional, filter-based, data-driven, hybrid | | Choose baseline SOC algorithm | No |
| 3 | Enhanced SOC Estimation of Li-Ion Batteries with Real-Time Data Using ML Algorithms | Sci. Reports 14, 16036, 2024 | https://www.nature.com/articles/s41598-024-66997-9 | SOC from real-time measurements | | | Compares ML regressors (SVM, NN, ensembles, GPR) | | Framework for V, I, T to SOC | No |
| 4 | Towards an Intelligent BMS for EV Applications: Dataset Considerations, Algorithmic Approaches, and Future Trends | J. Energy Storage, 2024, DOI 10.1016/j.est.2024.113827 | https://doi.org/10.1016/j.est.2024.113827 | Fair comparison across datasets | | | Reviews open aging datasets, SOH methods | | Dataset selection | No |
| 5 | Research Progress in Fault Detection of Battery Systems: A Review | J. Energy Storage 98, 113079, 2024 | https://doi.org/10.1016/j.est.2024.113079 | Early fault detection | | | Reviews threshold, model-based, data-driven detection | | Map faults to signals | No |
| 6 | An Exhaustive Review of Battery Faults and Diagnostic Techniques for Real-World EV Safety | J. Energy Storage 99, 113234, 2024 | https://doi.org/10.1016/j.est.2024.113234 | Interacting fault types in real use | | | Fault categories and diagnostics | | Fault taxonomy | No |
| 7 | Realistic Fault Detection of Li-Ion Battery via Dynamical Deep Learning | Nature Commun. 14, 5940, 2023 | https://www.nature.com/articles/s41467-023-41226-5 | Anomaly detection with scarce labelled failures | Real EV data, dataset released (check size claims) | Dynamical autoencoder | Anomaly detector plus released data | | Time-series prep, real dataset | No |
| 8 | Recent Advances in Model-Based Fault Diagnosis for Li-Ion Batteries: A Comprehensive Review | Renew. Sustain. Energy Rev., DOI 10.1016/j.rser.2024.114922 | https://doi.org/10.1016/j.rser.2024.114922 | Model uncertainty in diagnosis | | | Reviews models, observers, fault estimation | | Physics-based alternative to ML | No |
| 9 | Highly Available Li-Ion Batteries Sensors Readings Prediction Framework | IEEE Access 13, 99192-99202, 2025 | https://doi.org/10.1109/ACCESS.2025.3577133 | Missing/corrupted sensor readings | V, I, T | LSTM reconstruction | Reconstruct faulty sensor readings | | Fault-tolerant monitoring: sensor vs real fault | No |
| 10 | State of Charge Estimation Techniques for Li-Ion Batteries: A Review | Energy Technology, DOI 10.1002/ente.202500542 | https://doi.org/10.1002/ente.202500542 | Methods vary by chemistry/temperature | | | Reviews data-driven and hybrid SOC | | Final SOC method choice | No |

## Additional papers found by abstract search (also unverified)

| Topic | Title | Link |
|---|---|---|
| Distributed architecture | In-situ electronics and communications for intelligent energy storage | https://pmc.ncbi.nlm.nih.gov/articles/PMC9058845/ |
| Distributed architecture | Modular, Reconfigurable BESS: Design, Control, Experimentation | https://arxiv.org/abs/2301.05168 |
| Distributed SOC | Hybrid low-dimensional limiting SOC estimator for multi-cell batteries | https://arxiv.org/abs/2403.16555 |
| Distributed SOC | Partition-based UKF for reconfigurable pack state estimation | https://arxiv.org/abs/1709.07816 |
| CAN-based BMS | Advanced battery diagnostics using CAN-based BMS data with EKF | https://pmc.ncbi.nlm.nih.gov/articles/PMC12464234/ |
| SOC (EKF) | Parameter adaptive SOC estimation with improved EKF | https://pmc.ncbi.nlm.nih.gov/articles/PMC7952569/ |
| SOC (EKF) | Improved adaptive H-infinity EKF, online SOC | https://arxiv.org/abs/2304.07748 |
| SOC (EKF) | eXogenous Kalman Filter for SOC in EVs | https://arxiv.org/abs/1810.09014 |
| Fault | Model-Based Fault Diagnosis for Li-ion Batteries: Comprehensive Review | https://arxiv.org/abs/2401.16682 |
| Fault | Sensor-Fault-Estimation Method for Li-ion Batteries in EVs | https://pmc.ncbi.nlm.nih.gov/articles/PMC10537895/ |
| Fault | Optimal Sensor Placement for Fault Detection and Isolation | https://arxiv.org/abs/2008.10533 |
| Balancing | Novel active cell balancing topology, 96 cells in 10 modules | https://pmc.ncbi.nlm.nih.gov/articles/PMC11316807/ |

## Industry references

- TI white paper SLYY197, Wired vs. Wireless Communications in EV Battery Management: https://www.ti.com/document-viewer/lit/html/SLYY197
- TI reference design TIDUF92, Automotive High-Voltage BMS: https://training-dev.ti.com/cn/lit/pdf/tiduf92

## Note on novelty

A contribution claimed by a paper is not automatically novel in the patent sense. Our own gap must be checked against papers and patent databases before we rely on it.
