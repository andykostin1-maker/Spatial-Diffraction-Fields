# PUBLICATION_AUDIT

## Audit Intent

This audit defines what the repository can claim publicly, what is explicitly out of scope, and what evidence is required for stronger claims.

## Claim Taxonomy

### A. Supported in current release

The following claims are supported by the current code-and-artifact package:

- Scalar ASM propagation workflow
- Differentiable native K-pass optical operator (behavioral parameterization)
- Simulated WDM tensor execution path
- Simulated noise-aware training and perturbation analysis
- Simulated closed-loop scalar calibration flow
- Generic topology export to GDS/OASIS-like artifacts
- Reproducibility artifacts (reports, manifests, scripts)

### B. Not supported in current release

The following claims are **not** supported and must not be implied:

- Fabricated optical NPU throughput/latency/efficiency claims
- Measured TOPS/W or silicon power-performance claims
- Foundry DRC/LVS sign-off completion
- Proprietary PDK compatibility assertions
- Full-wave sign-off equivalence for all critical structures
- Production yield, reliability, or qualification claims

## Evidence Mapping

| Claim Type | Minimum Evidence Required |
|---|---|
| Simulation result | Scripted reproduction path + artifact output + parameter declaration |
| Architecture feasibility | End-to-end model description + benchmark context + known limitations |
| Calibration effectiveness | Raw vs calibrated error statistics under declared perturbations |
| Layout/topology generation | Deterministic geometry export + rule pre-check report |
| Reproducibility | Versioned manifest + deterministic command set |

## Communication Guardrails

1. Clearly label all numerical metrics as simulation-derived unless measured on hardware.
2. Disclose dataset scale and benchmark limits near reported model metrics.
3. Separate feasibility results from fabrication readiness statements.
4. Avoid wording that implies foundry qualification without PDK-bound sign-off evidence.
5. Include explicit "out of scope" sections in external summaries.

## Reviewer Checklist

Use this checklist before publishing external communication:

- [ ] All performance numbers are tagged as simulated or measured
- [ ] Any measured claim has traceable raw data and methodology
- [ ] No statements imply foundry sign-off unless DRC/LVS evidence is attached
- [ ] Limitations and assumptions are stated near key figures
- [ ] Reproduction commands and artifact paths are provided
- [ ] Security/privacy/IP disclosures contain no confidential data

## Disclosure Template

> This repository presents a simulation-based research prototype and reproducible engineering artifacts. Results should be interpreted as algorithmic and architectural feasibility under the stated assumptions. Fabrication claims require foundry-qualified PDK workflows, sign-off checks, and measured silicon data.
