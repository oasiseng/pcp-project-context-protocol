# Plans as a Product — Problem Definition & Scaffold

This document defines the problem, product intent, and execution scaffold for turning permit drawings into a field-usable construction product.

## 1) Problem Definition

### Current reality (single-family residential)
- Plans are frequently optimized for permit approval, not field execution.
- Drafters and designers may copy legacy habits that increase ambiguity or omit build-sequence context.
- Contractors buy plans for permitting; once approved, drawings are often underused during construction.
- Engineers inherit downstream risk: RFIs, failed inspections, rework, delays, and liability from misinterpretation/noncompliance.

### Root causes
- **Audience mismatch:** permit reviewers, builders, inspectors, and engineers need different signal density.
- **Information architecture issues:** critical details are buried, inconsistent, or disconnected from sequence.
- **No execution UX standard:** most plan sets are not explicitly designed for readability, cognition, and jobsite conditions.
- **Weak feedback loop:** field errors rarely flow back into drafting standards as measurable improvements.

### Cost of the problem
- Permit cycle delays and extra comments.
- Jobsite errors and unsafe improvisation.
- Higher engineering review burden and slower issue resolution.
- Margin loss from rework and schedule slippage.

## 2) Product Intent

Create a **Plan Product System** where drawings are both:
1. **Permit-valid** (regulatory completeness), and
2. **Build-operational** (clear, sequence-aware, low-friction for crews).

### Product thesis
A plan set should function like a guided operating system for construction, not just a compliance packet.

### Success outcomes
- Faster permit approvals with fewer correction cycles.
- Fewer field interpretation errors and RFIs.
- Better inspection pass rates.
- Less engineering firefighting and clearer accountability.

## 3) Design Principles (for every plan sheet)

1. **Clarity over density** — prioritize decision-critical information.
2. **Sequence-aware communication** — show build order and dependency explicitly.
3. **Cognitive ergonomics** — optimize typography, contrast, grouping, and scan paths.
4. **Role-based readability** — make the same sheet useful for reviewer, foreman, installer, and inspector.
5. **Closed-loop learning** — every field issue updates future standards.

## 4) Repo Direction: This Repo vs New Repo

Use this repository as the strategic home **for now**, because PCP already supports machine-readable project context and deliverable definitions.

### Keep this repo if
- You want a standards-first system connecting requirements, workflows, and QA gates.
- You want to automate intake, review, and deliverable generation using PCP artifacts.
- You want traceability from problem -> standard -> project payload.

### Start a new repo only if
- You need a separate product codebase (e.g., dedicated SaaS app with UI/backend).
- You need different licensing or governance from PCP core.

### Recommended approach
- Keep strategy/specs in this repo now.
- If software product scope grows, spin out an implementation repo later and keep this as the protocol/standards source.

## 5) Scope for Phase 1 (Pilot): Lanai Addition

Use a lanai addition as the first test case to validate the method.

### Pilot objective
Prove that a redesigned plan packet improves permit and field execution outcomes versus a traditional packet.

### Pilot deliverables
- **Plan Product Brief:** user roles, risks, and intended behaviors.
- **Sheet Architecture Spec:** standardized sheet order, labels, and visual hierarchy.
- **Execution Layer:** step-by-step install sequence mapped to sheets/details.
- **Inspection Layer:** explicit pre-inspection and final inspection checkpoints.
- **Issue Feedback Log:** structured capture of RFI/inspection/jobsite errors.

### Pilot metrics
- Permit cycle time and number of correction rounds.
- Number of RFIs per project.
- Inspection pass/fail rate on first attempt.
- Rework incidents tied to drawing ambiguity.
- Engineer review hours per project.

## 6) PCP Mapping (how this fits existing repo)

Represent the Plan Product System as PCP context and deliverable modules:

- Add/extend a project type for lanai additions.
- Add standardized deliverables for execution-oriented sheet packages.
- Add QC workflow gates for permit and field-readiness checks.
- Add role-specific agent instructions for drafting, review, and issue triage.

This allows consistent generation of project-ready, role-aware plan requirements.

## 7) 30/60/90-Day Build Plan

### First 30 days
- Define lanai pilot standard and baseline metrics.
- Draft the first “field-first” sheet architecture.
- Build review checklist for permit + constructability.

### By 60 days
- Run pilot projects through the new packet.
- Collect permit comments, RFIs, and inspection outcomes.
- Refine visual and sequencing standards.

### By 90 days
- Publish v1 Plan Product Standard.
- Create repeatable PCP templates for additional small residential scopes.
- Decide whether to spin out a dedicated product repo/application.

## 8) Immediate Next Actions

1. Author a lanai-specific PCP example payload under `examples/`.
2. Add a reusable “Plan Product” deliverable module under `library/`.
3. Define a field-issue taxonomy (ambiguity, sequencing, missing detail, code conflict).
4. Establish a weekly review loop to feed real project issues into standards updates.

---

This scaffold is intentionally practical: start with one scope, instrument outcomes, and improve the standard from measurable field results.
