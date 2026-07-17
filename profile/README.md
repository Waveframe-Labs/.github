<p align="center">
  <img src="https://raw.githubusercontent.com/Waveframe-Labs/.github/main/assets/branding/canon_wf_logo_extended.png" width="700" alt="Waveframe Labs">
</p>

# Waveframe Labs

**Governance infrastructure that prevents unsafe AI and automated actions from reaching production.**

AI can propose anything. Waveframe determines whether the proposed action is allowed to execute.

> We stop bad AI actions in one function call.

---

## The Product

Waveframe is an integrated governance and enforcement platform with distinct surfaces for governance teams, developers, operators, and auditors.

```text
Existing policy, SOP, or authority source
                  ↓
          Ledger Workspace
                  ↓
        Compiled authority
                  ↓
          Waveframe Cloud
                  ↓
          Waveframe Guard
                  ↓
              CRI-CORE
                  ↓
          ALLOW / BLOCK
                  ↓
        Production system
                  ↓
          Guard Inspector
```

- **Ledger Workspace** turns organizational policy into governed, publishable authority.
- **Waveframe Cloud** distributes immutable authority and preserves durable execution evidence.
- **Waveframe Guard** gives developers a simple runtime enforcement boundary.
- **CRI-CORE** deterministically decides whether a proposed mutation is admissible.
- **Guard Inspector** explains decisions, authority, and evidence to operators and auditors.

Guard is the developer adoption entry point. Ledger Workspace is the governance and enterprise expansion surface.

---

## Start With Guard

```bash
pip install waveframe-guard
```

```python
from waveframe_guard import Guard

guard = Guard.local(
    authority="finance-policy@1.0.0"
)
```

Guard loads published authority, constructs the governed proposal, invokes deterministic enforcement, blocks inadmissible execution, and preserves decision evidence.

Runtime enforcement remains local-first so a Cloud outage does not silently remove the execution boundary.

---

## How Waveframe Works

1. A governance team starts with an existing policy, procedure, delegation-of-authority document, or other authority source.
2. Ledger Workspace guides the team through normalization, diagnostics, compilation, review, and publication.
3. The published authority receives a stable identity, version, and cryptographic hash.
4. Waveframe Cloud distributes that authority to approved environments.
5. An application or agent proposes an action through Waveframe Guard.
6. Guard constructs a canonical proposal and submits it to CRI-CORE.
7. CRI-CORE returns the kernel-owned `commit_allowed` decision.
8. Guard either executes the action or prevents it from reaching the production mutation boundary.
9. Decision evidence is preserved for replay, inspection, and audit.

The system is model-agnostic. Proposed actions may originate from AI agents, traditional automation, applications, or human-operated workflows.

---

## Open Infrastructure

| Repository | Purpose |
| --- | --- |
| [Waveframe Guard](https://github.com/Waveframe-Labs/Waveframe-Guard) | Developer-facing runtime enforcement SDK |
| [CRI-CORE](https://github.com/Waveframe-Labs/CRI-CORE) | Deterministic execution-boundary enforcement kernel |
| [Contract Compiler](https://github.com/Waveframe-Labs/CRI-CORE-Contract-Compiler) | Human governance to deterministic compiled authority |
| [Proposal Normalizer](https://github.com/Waveframe-Labs/CRI-CORE-Proposal-Normalizer) | Canonical proposal construction and binding |
| [Governance Ledger](https://github.com/Waveframe-Labs/Governance-Ledger) | Authority preparation and publication infrastructure |

These repositories provide the local developer path, deterministic protocols, and inspectable enforcement foundation.

---

## Commercial Platform

| Product | Role |
| --- | --- |
| **Ledger Workspace** | Collaborative governance authoring, review, lifecycle, and publication |
| **Waveframe Cloud** | Authority distribution, organizational controls, and durable evidence |
| **Guard Inspector** | Decision, authority, receipt, and replay inspection |
| **Multi-tenant Operations** | Identity, tenancy, access control, supportability, and enterprise administration |

The commercial product is the integrated Waveframe platform—not any single repository in isolation.

---

## Governance Foundation

Waveframe's institutional governance and methodology remain separate from runtime product responsibilities.

| Repository | Authority |
| --- | --- |
| [Aurora Research Initiative](https://github.com/Waveframe-Labs/Aurora-Research-Initiative) | Governance authority and institutional accountability |
| [Neurotransparency Doctrine](https://github.com/Waveframe-Labs/Neurotransparency-Doctrine) | Epistemic doctrine and human decision ownership |
| [Neurotransparency Specification](https://github.com/Waveframe-Labs/Neurotransparency-Specification) | Structural compliance requirements |
| [Aurora Workflow Orchestration](https://github.com/Waveframe-Labs/Aurora-Workflow-Orchestration) | Governed workflow methodology |

These sources define governance expectations. Runtime products operationalize and enforce compiled authority without redefining it.

---

## Core Invariants

- The enforcement decision occurs before the production mutation.
- `commit_allowed` is owned by the enforcement kernel, not reconstructed by callers.
- Guard never compiles natural-language policy during runtime enforcement.
- Published authority is bound by identity, version, and cryptographic hash.
- Blocked actions do not reach the governed execution function.
- Local enforcement continues during Cloud unavailability.
- Cloud preserves evidence but does not replace the local execution decision.
- Inspector explains recorded decisions but does not rewrite them.

---

## Example

An AI system proposes reallocating **$2 million** between cost centers.

Without an execution boundary, the proposal may reach the financial system before a governance failure is detected.

With Waveframe:

```text
Proposal received
      ↓
Authority resolved and verified
      ↓
Required approval missing
      ↓
commit_allowed = False
      ↓
Execution blocked
      ↓
Evidence preserved for inspection
```

The action never reaches the financial mutation boundary.

---

## Compatibility

Version compatibility and dependency requirements are maintained at [waveframelabs.org/compatibility.html](https://waveframelabs.org/compatibility.html).

## Links

- [Waveframe Labs](https://waveframelabs.org)
- [Organization repositories](https://github.com/Waveframe-Labs)
- [ORCID](https://orcid.org/0009-0006-6043-9295)
- [swright@waveframelabs.org](mailto:swright@waveframelabs.org)

---

<div align="center">
  <sub>© 2026 Waveframe Labs</sub>
</div>
