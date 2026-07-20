<p align="center">
  <img src="https://raw.githubusercontent.com/Waveframe-Labs/.github/main/assets/branding/canon_wf_logo_extended.png" width="700" alt="Waveframe Labs">
</p>

# Waveframe Labs

**Deterministic execution governance for AI and automated systems.**

AI can propose anything. Waveframe determines whether the proposed action is allowed to execute.

> We stop bad AI actions in one function call.

---

## The Product

Waveframe is an integrated governance and enforcement platform that turns organizational authority into deterministic controls applied before sensitive actions reach production.

```text
Policy, SOP, or authority source
                ↓
        Ledger Workspace
                ↓
        Waveframe Ledger
 normalize → diagnose → review → publish
                ↓
      Versioned authority bundle
                ↓
        Waveframe Cloud
 distribute authority + preserve evidence
                ↓
        Waveframe Guard
                ↓
            CRI-CORE
                ↓
          ALLOW / BLOCK
                ↓
        Production system
                ↓
 Evidence → Cloud → Guard Inspector
```

- **Ledger Workspace** gives governance teams a collaborative surface for authoring, review, approval, lifecycle, and publication.
- **Waveframe Ledger** converts governed source material into deterministic, reviewable, publishable authority.
- **Waveframe Cloud** distributes immutable authority and preserves durable execution evidence.
- **Waveframe Guard** gives developers a local-first runtime enforcement boundary.
- **CRI-CORE** deterministically decides whether a proposed action is admissible.
- **Guard Inspector** explains decisions, authority, receipts, replay, and continuity to operators and auditors.

Guard is the developer adoption entry point. Ledger Workspace is the governance and enterprise expansion surface. The commercial product is the integrated Waveframe platform, not any repository in isolation.

---

## Start With Guard

```bash
pip install waveframe-guard
```

```python
from waveframe_guard import Guard

guard = Guard.local(workspace=".guard-local")

@guard.protect(authority="finance-policy@1.0.0")
def protected_action(execution_request):
    return perform_sensitive_action(execution_request)
```

Guard resolves and verifies published authority, constructs the governed proposal, invokes deterministic enforcement, blocks inadmissible execution, and preserves decision evidence.

Runtime enforcement remains local-first. Cloud unavailability does not silently remove the execution boundary.

---

## How Waveframe Works

1. A governance team starts with an existing policy, procedure, delegation-of-authority document, or other authority source.
2. Ledger Workspace guides normalization, diagnostics, review, approval, and publication.
3. Waveframe Ledger publishes a deterministic `authority_bundle.v1` with a stable identity, explicit version, lineage, and cryptographic hashes.
4. Waveframe Cloud stores and distributes the published authority to approved environments.
5. An application, agent, automation, or user proposes an action through Waveframe Guard.
6. Guard binds the action, actor, authority, artifacts, and runtime context into a canonical proposal.
7. CRI-CORE returns the kernel-owned `commit_allowed` decision and complete stage trace.
8. Guard invokes the protected function only when execution is allowed.
9. Decision evidence is written locally, preserved to Cloud, and made inspectable and replayable through Guard Inspector.

Waveframe is model-agnostic. It governs proposed actions rather than depending on how those actions were generated.

---

## Open Infrastructure

| Repository | Purpose |
| --- | --- |
| [Waveframe Guard](https://github.com/Waveframe-Labs/Waveframe-Guard) | Developer-facing local runtime enforcement SDK |
| [CRI-CORE](https://github.com/Waveframe-Labs/CRI-CORE) | Deterministic execution-boundary enforcement kernel |
| [Contract Compiler](https://github.com/Waveframe-Labs/cricore-contract-compiler) | Structured governance to deterministic compiled authority |
| [Proposal Normalizer](https://github.com/Waveframe-Labs/proposal-normalizer) | Canonical proposal construction and binding |
| [Waveframe Ledger](https://github.com/Waveframe-Labs/Waveframe-Ledger) | Governance normalization, diagnostics, publication, lineage, and replay |

These repositories provide the inspectable local developer path and deterministic protocol foundation.

---

## Commercial Platform

| Product | Primary user | Responsibility |
| --- | --- | --- |
| **Ledger Workspace** | Governance, risk, and compliance teams | Collaborative authority authoring, review, lifecycle, and publication |
| **Waveframe Cloud** | Platform and operations teams | Authority distribution, tenancy, durable evidence, receipts, replay, and continuity |
| **Guard Inspector** | Operators, investigators, and auditors | Decision explanation, evidence inspection, replay, and runtime chronology |
| **Multi-tenant Operations** | Enterprise administrators | Identity, access control, organization isolation, supportability, and administration |

The hosted platform creates operational value around the open deterministic foundation without moving the runtime execution decision into Cloud.

---

## Governance Foundation

Waveframe's institutional governance and methodology remain separate from runtime product responsibilities.

| Repository | Authority |
| --- | --- |
| [Aurora Research Initiative](https://github.com/Waveframe-Labs/Aurora-Research-Initiative) | Governance authority and institutional accountability |
| [Neurotransparency Doctrine](https://github.com/Waveframe-Labs/Neurotransparency-Doctrine) | Epistemic doctrine and human decision ownership |
| [Neurotransparency Specification](https://github.com/Waveframe-Labs/Neurotransparency-Specification) | Structural compliance requirements |
| [Aurora Workflow Orchestration](https://github.com/Waveframe-Labs/Aurora-Workflow-Orchestration) | Governed workflow methodology |

These sources define governance expectations. Runtime products operationalize and enforce published authority without redefining it.

---

## Core Invariants

- Enforcement occurs before the production mutation.
- `commit_allowed` is owned by CRI-CORE, not reconstructed by callers.
- Guard never compiles natural-language policy during runtime enforcement.
- Runtime authority references are explicit and versioned.
- Published authority is bound by identity, version, lineage, and cryptographic hash.
- Blocked actions do not reach the protected execution function.
- Local enforcement continues during Cloud unavailability.
- Cloud distributes authority and preserves evidence but does not decide runtime admissibility.
- Inspector explains recorded outcomes but does not rewrite enforcement semantics.

---

## Example

An AI system proposes reallocating **$2 million** between cost centers.

```text
Proposal received
      ↓
Authority resolved and verified
      ↓
Required CFO approval missing
      ↓
commit_allowed = False
      ↓
Protected transfer function is not invoked
      ↓
Evidence preserved for inspection and replay
```

The defining property is not that Waveframe generated an alert. The financial mutation never occurred.

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
