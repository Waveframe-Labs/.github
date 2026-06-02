<p align="center">
  <img src="https://raw.githubusercontent.com/Waveframe-Labs/.github/main/assets/branding/canon_wf_logo_extended.png" width="700">
</p>

# Waveframe Labs

Deterministic execution-governance infrastructure for AI and automated systems.

Most systems:

* monitor behavior
* generate alerts
* or audit after execution

Waveframe focuses on something else:

> determining whether a proposed action is allowed to execute before it reaches production systems.

---

# Canonical Execution Flow

```text
Governance Source
        ↓
Governance-Ledger
        ↓
Contract Compiler
        ↓
Compiled Authority Contract
        ↓
Proposal Normalizer
        ↓
Canonical Proposal
        ↓
CRI-CORE
        ↓
COMMIT ALLOWED / BLOCKED
        ↓
Waveframe Guard
        ↓
Production System
```

Waveframe Cloud provides:

* authority distribution
* durable audit infrastructure
* registry coordination
* and receipt verification

---

# Start Here

### Install Waveframe Guard

```bash
pip install waveframe-guard
```

Waveframe Guard wraps runtime execution and enforces governance locally before actions execute.

---

# Minimal Runtime Example

```python
from waveframe_guard import install_guard, guard

install_guard(
    actor={
        "id": "user-1",
        "type": "human",
        "role": "intern"
    },
    contract_path="finance-policy.contract.json"
)

@guard
def transfer(amount):
    print(f"Transferred ${amount}")

transfer(100)
```

```text
Execution blocked:
required role not satisfied: manager
```

---

# Core Infrastructure Layers

## Governance Layer

### Governance-Ledger

Transforms governed source text into deterministic authority artifacts.

Provides:

* governance normalization
* semantic diagnostics
* publication gating
* lineage verification
* authority publication

---

## Compilation Layer

### CRI-CORE Contract Compiler

Compiles governance policy into deterministic contracts.

```bash
pip install cricore-contract-compiler
```

Compiled contracts define:

* authority requirements
* approval thresholds
* execution constraints
* invariants
* artifact requirements

---

## Proposal Layer

### Proposal Normalizer

Builds canonical proposal objects from:

* actors
* mutations
* contracts
* governance artifacts

```bash
pip install cricore-proposal-normalizer
```

---

## Enforcement Layer

### CRI-CORE

Deterministic execution-boundary enforcement kernel.

```bash
pip install cricore
```

CRI-CORE evaluates:

* contracts
* proposals
* runtime context

and returns:

```python
commit_allowed = True | False
```

If `False`, the action must not execute.

CRI-CORE does not:

* generate actions
* orchestrate workflows
* interpret governance meaning
* persist authority

It only determines:

> whether a proposed action is admissible at execution time.

---

## Runtime Layer

### Waveframe Guard

Developer-facing runtime enforcement SDK.

Guard:

* loads contracts
* wraps execution
* evaluates admissibility
* blocks invalid actions locally
* continues enforcement during Cloud outages

---

## Authority & Audit Layer

### Waveframe Cloud

Authority distribution and durable evidence infrastructure.

Cloud provides:

* contract registry distribution
* immutable authority artifacts
* audit ingestion
* durable receipts
* organizational coordination

Cloud does not:

* evaluate admissibility
* execute actions
* normalize governance

---

# Example Scenario

## Financial Governance

An AI proposes reallocating $2M between cost centers.

Without enforcement:
→ execution proceeds immediately

With Waveframe:
→ proposal evaluated against authority contract
→ missing approval detected
→ COMMIT BLOCKED

The action never executes.

---

# Core Repositories

| Repository          | Purpose                                       |
| ------------------- | --------------------------------------------- |
| Waveframe Guard     | Runtime execution enforcement SDK             |
| CRI-CORE            | Deterministic enforcement kernel              |
| Governance-Ledger   | Governance operationalization infrastructure  |
| Contract Compiler   | Governance contract compilation               |
| Proposal Normalizer | Canonical proposal construction               |
| Waveframe Cloud     | Authority distribution + audit durability     |
| Waveframe Schemas   | Canonical protocol and object schemas         |
| Waveframe Telemetry | Runtime telemetry and evidence infrastructure |
| Waveframe Stamp     | Artifact and metadata validation              |
| Waveframe pdf Forge | Publication and artifact generation           |

---

# Demonstrations

Repositories in this organization demonstrate:

* governed financial mutations
* execution-boundary enforcement
* approval threshold enforcement
* role separation
* admissibility replay
* runtime governance blocking

Each demo answers one question:

> does the proposed action execute or not?

---

# Compatibility

Version compatibility and dependency requirements are documented at:

https://waveframelabs.org/compatibility.html

---

# Licensing

| Category             | License         |
| -------------------- | --------------- |
| Tooling & Code       | Apache 2.0      |
| Documentation        | CC BY-NC-SA 4.0 |
| Governance & Methods | CC BY 4.0       |

---

# Links

Website — https://waveframelabs.org
ORCID — https://orcid.org/0009-0006-6043-9295
Contact — [swright@waveframelabs.org](mailto:swright@waveframelabs.org)

---

<div align="center">
  <sub>© 2026 Waveframe Labs</sub>
</div>
