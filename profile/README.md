---
title: "Waveframe Labs Organization Overview"
filetype: "documentation"
type: "non-normative"
domain: "infrastructure"
version: "1.1.0"
doi: "N/A"
status: "Active"
created: "2026-03-04"
updated: "2026-03-04"

author:
  name: "Shawn C. Wright"
  email: "swright@waveframelabs.org"
  orcid: "https://orcid.org/0009-0006-6043-9295"

maintainer:
  name: "Waveframe Labs"
  url: "https://waveframelabs.org"

license: "CC-BY-4.0"

copyright:
  holder: "Waveframe Labs"
  year: "2026"

ai_assisted: "partial"
---

<p align="center">
  <img src="../master-banner.png" alt="Waveframe Labs Banner" width="600">
</p>

# Waveframe Labs

Waveframe Labs develops governance and enforcement infrastructure for AI-assisted workflows and reproducible research systems.

Our work focuses on the **execution boundary** — the point where system state changes under regulatory, operational, or institutional risk.

Governance is only meaningful if that boundary is structurally enforced.

---

## What This Organization Contains

This organization hosts the governance framework, enforcement tooling,
validation utilities, and demonstration repositories that make up the
Waveframe governance stack.

---

# Core Infrastructure DOIs

Neurotransparency Doctrine (NTD)  
https://doi.org/10.5281/zenodo.17957384  

Neurotransparency Standard (NTS)  
https://doi.org/10.5281/zenodo.17809676  

Aurora Research Initiative (ARI)  
https://doi.org/10.5281/zenodo.17743096  

Aurora Workflow Orchestration (AWO)  
https://doi.org/10.5281/zenodo.17013612  

Stamp (Deterministic Artifact & Metadata Validator)  
https://doi.org/10.5281/zenodo.18436622  

---

# Architectural Layers

Waveframe Labs separates governance, method, enforcement, and validation into distinct layers. Enforcement and validation components are distributed as installable Python packages.

**Governance — ARI / NTS**  
Defines institutional authority boundaries, policy contracts, and AI disclosure requirements.

**Method — AWO**  
Defines structured workflow topology, role separation, manifests, and reproducibility guarantees.

**Enforcement — CRI-CORE**  
Deterministic transition-boundary enforcement engine that evaluates whether a declared state transition satisfies structural governance constraints before execution.

CRI-CORE is distributed as an installable Python package:
```
pip install cricore
```

**Validation — Stamp**
Schema-agnostic artifact and metadata validator producing deterministic diagnostics and machine-readable outputs.

Stamp validates artifact structure and metadata prior to enforcement and downstream publication processes.

Stamp is distributed as an installable Python package:
```
pip install waveframe-stamp
```
---

# Demonstration Repositories

Several repositories in this organization demonstrate how Waveframe governance infrastructure operates in practice.

Examples include:

- Claim lifecycle governance demonstrations
- Deterministic financial responsibility enforcement examples
- Artifact validation demonstrations

These projects illustrate how governance constraints can be enforced at the mutation boundary of operational workflows.

---

# Publication Tooling

Waveframe Forge provides tooling for generating Scholar-ready artifacts from governed Markdown sources.

Publication artifacts produced with this tooling are stored in the **Waveframe-Publications** repository.

---

# What This Organization Builds

Waveframe Labs develops infrastructure for:

- Atomic, auditable state transitions
- Explicit authority modeling
- Deterministic enforcement of declared contracts
- Cryptographic artifact integrity
- Machine-verifiable provenance

Policy definition, workflow structure, and execution enforcement are intentionally separated.

Policy sits above.  
Execution sits below.  

The enforcement kernel asks one question:

**"Can this transition commit safely?"**

---

# Core Repositories

| Layer | Project | Purpose |
|------|------|------|
| Governance | ARI | Institutional authority and governance constraints |
| Specification | NTS | Machine-verifiable AI disclosure requirements |
| Method | AWO | Structured workflow topology for governed research |
| Enforcement | CRI-CORE | Deterministic transition-boundary enforcement |
| Validation | Stamp | Artifact validation and diagnostics engine |

---

# Licensing

| Category | License |
|--------|--------|
| Governance & Methods (ARI, AWO) | CC BY 4.0 |
| Specification (NTS) | CC BY 4.0 |
| Tooling & Code (CRI-CORE, Stamp) | Apache 2.0 |
| Documentation | CC BY-NC-SA 4.0 |

All versioned releases include DOIs and cryptographic provenance artifacts where applicable.

---

# Links

**Website** — https://waveframelabs.org  
**ORCID** — https://orcid.org/0009-0006-6043-9295  
**Contact** — swright@waveframelabs.org  

---

© 2026 Waveframe Labs · Governance Infrastructure for AI-Assisted Workflows
