---
title: "Waveframe Labs Organization Overview"
filetype: "documentation"
type: "non-normative"
domain: "infrastructure"
version: "1.1.1"
doi: "N/A"
status: "Active"
created: "2026-03-04"
updated: "2026-03-29"

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

**Waveframe Labs builds systems that stop unsafe AI actions before they execute.**

As AI systems become capable of taking real-world actions — moving money, deploying code, approving decisions — most systems still rely on monitoring, logging, or after-the-fact auditing.

But none of those control the moment that actually matters:

**execution.**

Waveframe focuses on the **execution boundary** — the point where a proposed action becomes real.

At that boundary, the system must decide:

- allow the action  
- or block it before it happens  

---

## What This Organization Contains

This organization contains the infrastructure required to enforce that decision.

It includes:

- deterministic enforcement tooling  
- validation utilities  
- governance and contract definition layers  
- demonstration repositories showing real-world scenarios  

Together, these components form a system that ensures:

> **no action executes unless it passes validation**

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

Waveframe Labs separates governance, method, enforcement, and validation into distinct layers.

Each layer exists to support a single outcome:

**deterministic control over execution.**

**Governance — ARI / NTS**  
Defines authority, policy contracts, and AI disclosure requirements.

**Method — AWO**  
Defines workflow structure, role separation, and reproducibility requirements.

**Enforcement — CRI-CORE**  
Deterministic execution control layer that evaluates whether a proposed action satisfies structural constraints before it is allowed to execute.

CRI-CORE is distributed as an installable Python package:
```

pip install cricore

```

**Validation — Stamp**  
Validates artifact structure and metadata before enforcement.

Stamp is distributed as an installable Python package:
```
pip install waveframe-stamp
```

---

# Demonstration Repositories

Several repositories in this organization demonstrate how execution control works in practice.

Examples include:

- AI-driven financial actions blocked due to missing approval  
- governed claim lifecycle transitions  
- structural validation and integrity enforcement scenarios  

These demonstrations show a simple idea:

> **an action either passes validation and executes — or it doesn’t**

---

# Publication Tooling

Waveframe Forge provides tooling for generating structured, reproducible artifacts from governed Markdown sources.

Publication artifacts are stored in the **Waveframe-Publications** repository.

---

# What This Organization Builds

Waveframe Labs develops systems for:

- controlling AI-driven execution  
- enforcing role separation and authority  
- validating actions before they occur  
- ensuring cryptographic integrity of execution artifacts  
- producing auditable, machine-verifiable outcomes  

Policy definition, workflow structure, and execution enforcement are intentionally separated.

Policy sits above.  
Execution sits below.  

The enforcement layer answers one question:

**"Should this action be allowed to execute?"**

---

# Core Repositories

| Layer | Project | Purpose |
|------|------|------|
| Governance | ARI | Institutional authority and governance constraints |
| Specification | NTS | Machine-verifiable AI disclosure requirements |
| Method | AWO | Structured workflow topology for governed processes |
| Enforcement | CRI-CORE | Deterministic execution control layer |
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

© 2026 Waveframe Labs · Deterministic Control for AI Execution
