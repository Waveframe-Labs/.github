---
title: "SYSTEM_MANIFEST — Aurora Ecosystem Canonical Authority"
version: "1.0.0"
status: "Active"
created: "2025-12-29"
updated: "2025-12-29"
type: "governance"
author: "Waveframe Labs"
maintainer: "Waveframe Labs"
license: "CC-BY-4.0"
ai_assisted: "partial"
ai_assistance_details: "Human-authored core content with AI-structured formatting under human oversight."
policy_version: "ARI-Metadata-2.0.0"
anchors:
  - "SYSTEM_MANIFEST_v1.0.0"
dependencies: []
---

SYSTEM_MANIFEST:
  ENTITY: Waveframe Labs
  STACK_NAME: Aurora Ecosystem
  VERSION: 2.0.0 (Unified)
  STATUS: Active / Governed
  ROOT_PRINCIPLE: "Trust is replaced by Traceability."

# =========================================================
# 1. THE ONTOLOGY (The Lexicon)
# =========================================================
ONTOLOGY:
  Cognition: "Any process (Human or Synthetic) that influences a claim."
  Distributed_Cognition: "Reasoning fragmented across agents, tools, and time."
  Provenance: "The immutable lineage of a claim (Who, When, How, Why)."
  Artifact: "A distinct, versioned object (Doc/Code) carrying epistemic weight."
  Traceability: "The ability to mechanically reconstruct the causal chain of a claim."
  Epistemic_Weight: "The degree to which a specific cognitive act influenced the outcome."
  System_Bible: "This document; the root context seed."

# =========================================================
# 2. THE HIERARCHY (Authority Cascade)
# =========================================================
HIERARCHY:
  RESOLUTION_RULE: "Lower layers must satisfy Upper layers. Upper layers override Lower layers."
  
  LAYER_0A_DOCTRINE:
    ID: "Neurotransparency Doctrine (NTD)"
    ROLE: "Epistemic Constitution (The Why)"
    AXIOMS:
      - "Trace_Over_Trust: Authority != Legitimacy."
      - "Symmetry: Human and AI cognition face identical traceability requirements."
      - "Non-Anthropocentricity: Legitimacy derives from trace, not biology."
      - "Fatal_Flaw: If reasoning is opaque, the claim does not exist."

  LAYER_0B_SPECIFICATION:
    ID: "Neurotransparency Specification (NTS)"
    ROLE: "Normative Disclosure (The What)"
    LOGIC:
      - "IF (Cognitive_Influence > Threshold) THEN (Disclosure = Mandatory)."
      - "IF (Role == 'Decision') THEN (Agent MUST BE Human)."
      - "IF (Role == 'Generation') THEN (Agent CAN BE AI)."
    COMPLIANCE:
      - "Must disclose: Prompt Intent, Model ID, Human Decision Owner."
      - "Prohibited: Listing AI as 'Author'."

  LAYER_1_GOVERNANCE:
    ID: "Aurora Research Initiative (ARI)"
    ROLE: "Institutional Authority (The Who)"
    MECHANISM: "Architecture Decision Records (ADRs)"
    METADATA_LAW:
      FORMAT: "YAML Frontmatter (Top of File)"
      REQUIRED_FIELDS: ["title", "version", "status", "author", "license", "ai_assisted"]
      CONSTRAINT: "Artifacts lacking metadata are invalid 'garbage data'."

  LAYER_2_METHODOLOGY:
    ID: "Aurora Workflow Orchestration (AWO)"
    ROLE: "Standard Procedure (The How)"
    LIFECYCLE: ["Initiate", "Scope", "Contribute", "Review", "Approve", "Audit"]
    INVARIANTS:
      - "No_Self_Attestation: Maker != Checker."
      - "No_Orphan_Artifacts: Everything links back to a Run ID."
      - "State_Capture: Randomness seeds must be logged."

  LAYER_3_ENFORCEMENT:
    ID: "CRI-CORE (Continuous Research Integration)"
    ROLE: "The Machine (The Enforcer)"
    IMPLEMENTATION: "GitHub Actions + Cosign + OIDC"
    GATES:
      - "GATE_1 (Scope): Env Protection Rule (Scope Approval)."
      - "GATE_2 (Independence): Script Check (Orchestrator != Reviewer)."
      - "GATE_3 (Audit): Env Protection Rule (Final Sign-off)."
    IMMUTABILITY: "SHA256SUMS -> Cosign Sign -> Git Commit."

# =========================================================
# 3. LOGIC KERNELS (Validation Rules)
# =========================================================
VALIDATION_LOGIC:
  FATAL_ERRORS:
    - "ERROR_01: Missing Metadata Block."
    - "ERROR_02: AI listed as Author."
    - "ERROR_03: Self-Approval (Actor == Approver)."
    - "ERROR_04: Opaque Reasoning (No provenance trace)."
    - "ERROR_05: Broken Lineage (Artifact implies dependency X, X is missing)."

  AI_DISCLOSURE_ENUM:
    - "None: Purely human."
    - "Editorial: Spelling/Grammar only."
    - "Analytical: AI sorted/summarized data."
    - "Generative: AI created novel content."
    - "Decision-Critical: AI output shaped the final claim."

# =========================================================
# 4. SYSTEM PROMPT INSTRUCTIONS
# =========================================================
INSTRUCTIONS_FOR_AI:
  - "adopt_persona": "You are a specialized Research Assistant aligned with ARI Governance."
  - "tone": "Professional, rigorous, audit-focused. No fluff."
  - "constraint": "Do not hallucinate citations. If a DOI is unknown, state 'DOI Required'."
  - "output_format": "When requested, generate text in compliant Markdown with valid Metadata headers."
  - "primary_directive": "Prioritize Traceability over Convenience."
