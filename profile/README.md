---
title: "Waveframe Labs Organization Overview"
filetype: "documentation"
type: "non-normative"
domain: "infrastructure"
version: "1.2.0"
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

As AI systems begin to take real-world actions — moving money, deploying code, approving decisions — most systems still rely on monitoring or auditing.

But those happen before or after execution.

They do not control the moment that actually matters:

**execution.**

Waveframe focuses on the **execution boundary** — the point where a proposed action becomes real.

At that boundary, the system must decide:

- allow the action  
- or block it before it happens  

---

## Start Here (Minimal Stack)

Waveframe provides a minimal, executable pipeline for controlling AI-driven actions.

### 1. Enforcement (Core)

```
pip install cricore
```

Deterministically decides whether an action is allowed to execute.

---

### 2. Supporting Layers

```
pip install cricore-proposal-normalizer
```

Converts actions into structured inputs for enforcement.

```
pip install cricore-contract-compiler
```

Compiles governance rules into enforceable contracts.

---

### 3. Demo (Proof)

**Finance Governance Demo**

An AI attempts to move $2M:

- Without enforcement → action executes  
- With CRI-CORE → action is blocked  

→ See: `governed-mutation-pipeline-demo`

---

## What This Organization Contains

This organization contains the infrastructure required to enforce execution control:

- deterministic enforcement tooling  
- validation utilities  
- governance and contract definition layers  
- demonstration repositories  

Together, these components ensure:

> **no action executes unless it passes validation**

---

# Architectural Layers

Waveframe separates governance, method, enforcement, and validation into distinct layers.

Each layer supports a single outcome:

**deterministic control over execution**

**Governance — ARI / NTS**  
Defines authority, policy contracts, and AI disclosure requirements.

**Method — AWO**  
Defines workflow structure and role separation.

**Enforcement — CRI-CORE**  
Deterministic execution control layer.

**Validation — Stamp**  
Validates artifact structure and metadata before enforcement.

---

# Demonstration Repositories

Repositories in this organization show how execution control works in practice.

Examples include:

- financial actions blocked due to missing approval  
- governed lifecycle transitions  
- structural validation scenarios  

These demonstrations show:

> **an action either executes — or it doesn’t**

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

Stamp  
https://doi.org/10.5281/zenodo.18436622  

---

# What This Organization Builds

Waveframe Labs develops systems for:

- controlling AI-driven execution  
- enforcing role separation and authority  
- validating actions before they occur  
- ensuring cryptographic integrity  
- producing auditable outcomes  

Policy definition, workflow structure, and execution enforcement are separated.

Policy sits above.  
Execution sits below.  

The system answers one question:

**"Should this action be allowed to execute?"**

---

# Core Repositories

| Layer | Project | Purpose |
|------|------|------|
| Governance | ARI | Authority and governance constraints |
| Specification | NTS | AI disclosure requirements |
| Method | AWO | Workflow structure |
| Enforcement | CRI-CORE | Execution control |
| Validation | Stamp | Artifact validation |

---

# Licensing

| Category | License |
|--------|--------|
| Governance & Methods | CC BY 4.0 |
| Specification | CC BY 4.0 |
| Tooling & Code | Apache 2.0 |
| Documentation | CC BY-NC-SA 4.0 |

---

# Links

**Website** — https://waveframelabs.org  
**ORCID** — https://orcid.org/0009-0006-6043-9295  
**Contact** — swright@waveframelabs.org  

---

© 2026 Waveframe Labs · Deterministic Control for AI Execution
