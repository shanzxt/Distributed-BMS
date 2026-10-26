# Distributed Battery Management System

**Project title:** Develop a distributed Battery Management System for a multi-cell battery pack capable of monitoring cells, estimating SOC and performing fault management.

**Group 02:** Harshal Chaudhari, Shantanu Somwanshi, Presha Rane
**Guide:** KPIT Laboratory
**Institute:** COEP Technological University, Pune

## Goal

Build a distributed BMS: slave modules sense cell voltage and temperature and report over a shared bus (CAN) to a master that estimates SOC, detects faults and controls pack disconnect. The project follows the Software Development Life Cycle (SDLC) and aims to end in a patent filing or a conference publication.

## Status

| SDLC phase | Folder | Status |
|---|---|---|
| Stage 1: Literature, sensors, datasets, research gap | `docs/stage1/` | In progress |
| Requirements | `docs/requirements/` | Not started |
| Design | `docs/design/` | Not started |
| Implementation | `hardware/`, `firmware/`, `simulation/` | Not started |
| Testing | `tests/`, `docs/test-reports/` | Not started |
| Release and maintenance | Git tags | Not started |

## Repository layout

```
docs/stage1/      Stage 1 deliverables (see below)
hardware/         Schematics, PCB, BOM
firmware/         Slave and master firmware
simulation/       Battery models, SOC algorithms, test data scripts
tests/            Unit and integration tests
.github/          Issue templates
```

## Stage 1 deliverables

1. [Sensor selection report](docs/stage1/sensor-selection.md)
2. [Literature review matrix](docs/stage1/literature-matrix.md)
3. [Dataset assessment](docs/stage1/dataset-assessment.md)
4. [Research gap statement](docs/stage1/research-gap.md)

## Working rules

- `main` is protected by convention: work on a branch, open a pull request, have a teammate review.
- One GitHub Issue per deliverable or requirement.
- Tag a release at the end of each stage (`v0.1-stage1`, `v0.2-design`, ...).
- Nothing in this repo is claimed as novel until the research gap has been checked against prior papers and patents.

## Intellectual property note

We may file a patent. Public disclosure before filing can destroy novelty, so keep implementation details, algorithms and results out of public view until the team and the institute's IPR cell have decided. This repository should be **private** until then.
