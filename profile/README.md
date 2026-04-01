---
title: "Waveframe Labs Organization Overview"
filetype: "documentation"
type: "non-normative"
domain: "infrastructure"
version: "1.3.0"
doi: "N/A"
status: "Active"
created: "2026-03-04"
updated: "2026-04-01"

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

**What actually stops an AI system from executing a bad decision?**

Most systems:
- detect issues  
- log them  
- or audit after the fact  

But by the time that happens, the action has already executed.

**Waveframe Labs builds systems that decide whether an action is allowed to execute — before it happens.**

---

# Start Here

### Install the enforcement layer

```bash
pip install cricore
````

CRI-CORE evaluates a proposed action and returns:

```
commit_allowed = true | false
```

* `true` → action executes
* `false` → action is blocked

👉 This is the execution decision boundary.

---

# Minimal Pipeline

You can run CRI-CORE alone, or as part of a simple pipeline:

### 1. Structure the action

```bash
pip install cricore-proposal-normalizer
```

Converts an action into a structured input.

---

### 2. Define the rules

```bash
pip install cricore-contract-compiler
```

Compiles roles, approvals, and constraints into enforceable contracts.

---

### 3. Enforce execution

```bash
pip install cricore
```

Deterministically decides if the action executes.

---

# Example

**Finance scenario**

An AI proposes moving $2M between cost centers.

Without enforcement:
→ action executes

With CRI-CORE:
→ blocked due to missing approval

👉 See: `governed-mutation-pipeline-demo`

---

# What This Organization Contains

This organization provides the infrastructure required to control execution:

* enforcement tooling
* input normalization
* contract compilation
* validation utilities
* working demonstrations

The goal is simple:

> **no action executes unless it passes validation**

---

# Where CRI-CORE Fits

CRI-CORE is the final step before execution.

It does not:

* generate actions
* interpret meaning
* make policy decisions

It only answers:

> **Does this action execute or not?**

---

# Supporting Infrastructure (Optional)

These layers support enforcement but are not required to get started:

* **Stamp** — validates artifacts and metadata
* **AWO** — workflow structure
* **ARI / NTS** — governance and disclosure rules

---

# Demonstrations

Repositories in this organization show real execution control:

* blocked financial actions
* governed state transitions
* validation failures

Each demo shows:

> **an action either executes — or it doesn’t**

---

# Core Repositories

| Component           | Purpose                                   |
| ------------------- | ----------------------------------------- |
| CRI-CORE            | Execution decision layer                  |
| Contract Compiler   | Converts rules into enforceable contracts |
| Proposal Normalizer | Structures actions for evaluation         |
| Stamp               | Validates artifacts                       |

---

# Licensing

| Category             | License         |
| -------------------- | --------------- |
| Tooling & Code       | Apache 2.0      |
| Documentation        | CC BY-NC-SA 4.0 |
| Governance & Methods | CC BY 4.0       |

---

# Links

**Website** — [https://waveframelabs.org](https://waveframelabs.org)
**ORCID** — [https://orcid.org/0009-0006-6043-9295](https://orcid.org/0009-0006-6043-9295)
**Contact** — [swright@waveframelabs.org](mailto:swright@waveframelabs.org)

---

<div align="center">
  <sub>© 2026 Waveframe Labs — Independent Open-Science Research Entity</sub>
</div>
