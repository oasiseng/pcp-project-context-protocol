# PCP Specification (v0.1.0)

## 1. Purpose

The Project Context Protocol (PCP) defines a standard payload for project setup and execution. A PCP payload is expected to be machine-readable and operationally complete enough for both humans and agents.

## 2. Top-Level Contract

A valid PCP payload MUST include:
- `pcp_version`
- `project`
- `deliverables`
- `documents_required`
- `context_modules`

A payload MAY include:
- `workflows`
- `agents`
- `airtable`
- `metadata`

## 3. Data Model

### 3.1 `project`

Defines project identity and execution attributes.

Required fields:
- `id`
- `name`
- `type`
- `lifecycle_stage`
- `objective`

Recommended fields:
- `owner`
- `priority`
- `start_date`
- `target_date`
- `roles`

### 3.2 `deliverables`

List of output objects that must be completed.

Each deliverable should define:
- clear owner role
- status
- definition of done
- acceptance criteria
- dependency references when needed

### 3.3 `documents_required`

List of mandatory artifacts (plans, specs, runbooks, reports).

Each document should define:
- template or schema source
- responsible role
- stage due
- required/optional classification

### 3.4 `context_modules`

Reusable context packs that govern execution quality.

Examples:
- engineering standards
- QC checklists
- release criteria
- security policy packs
- optimization rubrics

### 3.5 `workflows`

Stage gates and checks controlling movement across project phases.

### 3.6 `agents`

Automation or bot definitions with explicit scope, inputs, outputs, and constraints.

### 3.7 `airtable`

Optional mapping from PCP entities to Airtable tables and fields.

## 4. Validation Rules

- IDs SHOULD be stable and lowercase kebab-case.
- Required arrays SHOULD contain at least one item for active projects.
- Dates SHOULD be ISO-8601 (`YYYY-MM-DD`).
- Unknown top-level fields SHOULD be rejected by strict validators.

## 5. Governance

- New fields require schema updates and example updates.
- Breaking changes require major version increments.
- Repository maintainers should keep migration notes per major change.
