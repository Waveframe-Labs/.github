<p align="center">
```
`<img src="../master-banner.png" alt="Waveframe Labs Banner" width="600">`{=html}
```{=html}
</p>

# Waveframe Labs

Waveframe Labs builds deterministic enforcement and validation
infrastructure for governed AI workflows.

We focus on the execution boundary --- the point where system state
changes under regulatory, operational, or institutional risk.

Governance is only meaningful if that boundary is structurally enforced.

---

## Core Infrastructure DOIs

Neurotransparency Doctrine (NTD)\
https://doi.org/10.5281/zenodo.17957384

Neurotransparency Standard (NTS)\
https://doi.org/10.5281/zenodo.17809676

Aurora Research Initiative (ARI)\
https://doi.org/10.5281/zenodo.17743096

Aurora Workflow Orchestration (AWO)\
https://doi.org/10.5281/zenodo.17013612

Stamp (Deterministic Artifact & Metadata Validator)\
https://doi.org/10.5281/zenodo.18436622

---

# Architectural Layers

Waveframe Labs separates governance, method, enforcement, and validation
into distinct layers:

Governance --- ARI / NTS\
Defines institutional authority boundaries, policy contracts, and AI
disclosure requirements.

Method --- AWO\
Defines structured workflow topology, role separation, manifests, and
reproducibility guarantees.

Enforcement --- CRI-CORE\
Deterministic transition-boundary enforcement engine.\
Validates that state changes satisfy declared contracts before they
commit.

Validation --- Stamp\
Schema-agnostic artifact and metadata validator.\
Emits deterministic diagnostics and machine-readable outputs for
downstream enforcement.

---

# What This Organization Builds

Waveframe Labs builds infrastructure for:

-   Atomic, auditable state transitions
-   Explicit authority modeling
-   Deterministic enforcement of declared contracts
-   Cryptographic artifact integrity
-   Machine-verifiable provenance

We do not collapse policy, authority, and execution into a single layer.

Policy sits above.\
Execution sits below.\
The enforcement kernel asks one question:

"Can this transition commit safely?"

---

# Core Repositories

  ------------------------------------------------------------------------
  Layer                         Project              Purpose
  ----------------------------- -------------------- ---------------------
  Governance                    ARI                  Institutional
                                                     authority and
                                                     governance
                                                     constraints

  Specification                 NTS                  Machine-verifiable AI
                                                     disclosure
                                                     requirements

  Method                        AWO                  Structured workflow
                                                     topology for governed
                                                     research

  Enforcement                   CRI-CORE             Deterministic
                                                     transition-boundary
                                                     enforcement

  Validation                    Stamp                Artifact validation
                                                     and diagnostics
                                                     engine
  ------------------------------------------------------------------------

---

# Licensing

  Category                           License
  ---------------------------------- -----------------
  Governance & Methods (ARI, AWO)    CC BY 4.0
  Specification (NTS)                CC BY 4.0
  Tooling & Code (CRI-CORE, Stamp)   Apache 2.0
  Documentation                      CC BY-NC-SA 4.0

All versioned releases include DOIs and cryptographic provenance
artifacts where applicable.

------------------------------------------------------------------------

# Links

Website --- https://waveframelabs.org\
ORCID --- https://orcid.org/0009-0006-6043-9295\
Contact --- swright@waveframelabs.org

------------------------------------------------------------------------

© 2026 Waveframe Labs · Governance Infrastructure for AI Workflows
