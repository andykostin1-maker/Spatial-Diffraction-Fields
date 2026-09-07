# POST_PDK_ROADMAP

## Purpose

This roadmap defines the qualification path from a behavioral research prototype to a foundry-qualified photonic hardware program.

## Current Baseline

- Modeling level: scalar ASM + behavioral emulation
- Topology level: generic scaffold geometry
- Validation level: software regression + simulated PVT/calibration
- Foundry readiness: **false**

## Gate-Based Qualification Plan

### Gate 1 — Optical Cell Physics Closure

**Objective:** Replace behavioral assumptions for critical optical cells with calibrated full-wave results.

**Scope:**
- Grating couplers
- Splitters/combiners
- PCM transition cells
- High-sensitivity routing structures

**Deliverables:**
- Full-wave simulation datasets (S-parameters, insertion loss, phase response)
- Reduced-order compact models for system-level integration
- Correlation report: behavioral vs full-wave deltas and accepted error bounds

### Gate 2 — PDK and Rule-Deck Integration

**Objective:** Move from generic layers to foundry-qualified layer mapping and sign-off rules.

**Scope:**
- PDK layer mapping for all optical/electrical layers used by the design
- DRC and LVS rule-deck integration
- Process corner definition and verification

**Deliverables:**
- PDK-bound layout database
- DRC clean reports
- LVS consistency reports
- Corner-aware geometry constraints (etch bias, line-edge roughness, CD variation)

### Gate 3 — Coupled Thermal-Optical Validation

**Objective:** Validate data-dependent thermal behavior under realistic workloads.

**Scope:**
- Time-dependent hotspot simulation
- Coupled optical + thermal transients
- Package-level boundary condition modeling

**Deliverables:**
- Transient thermal maps across representative workloads
- Phase/gain drift transfer functions vs temperature/time
- Compensation envelope for control and calibration loops

### Gate 4 — BSI/ROIC and Readout Chain Characterization

**Objective:** Replace idealized detector/readout assumptions with realistic electrical behavior.

**Scope:**
- TIA behavior and settling
- ADC non-linearity (INL/DNL)
- Offset, dark current, temporal noise, and crosstalk

**Deliverables:**
- Detector/readout behavioral models calibrated to characterized data
- End-to-end SNR and dynamic range budgets
- Readout-induced error decomposition report

### Gate 5 — Multi-Seed System Validation at Scale

**Objective:** Demonstrate statistical stability on larger public datasets and expanded configurations.

**Scope:**
- Larger corpus and broader workload coverage
- Multi-seed training/evaluation for native optical operators
- Robustness under wavelength/thermal/noise perturbations

**Deliverables:**
- Multi-seed benchmark tables with confidence intervals
- Failure-mode and sensitivity analysis
- Reproducibility package update with manifests and scripts

## Exit Criteria for Fabrication-Oriented Claims

Fabrication-oriented performance claims are deferred until all gates complete with traceable evidence:

1. Full-wave optical closure for critical cells
2. PDK-mapped DRC/LVS clean implementation
3. Coupled thermal-optical transient validation
4. Characterized BSI/ROIC readout model integration
5. Multi-seed reproducible system benchmarks
6. Measured silicon correlation where available

## Notes

- This document is an engineering qualification plan, not a fabrication claim.
- Until gate completion, project outputs remain simulation-driven research artifacts.
