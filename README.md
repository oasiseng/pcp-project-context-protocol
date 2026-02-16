# PCP: Project Context Protocol

PCP is an open, machine-readable protocol for defining how a project should run.

It standardizes:
- project type and execution model
- required deliverables
- required documents
- context libraries (engineering standards, QC checklists, policies)
- optimization rubrics (cycle time, quality, predictability, cost)
- bot/agent operating context
- Airtable mapping for operational use

The goal is simple: one shared project contract that humans and bots can both execute against.

## Why PCP

Most teams lose time because project context lives across docs, chat, and memory. PCP turns that context into a single protocol payload so work can be launched, audited, and automated consistently.

## Core Concepts

- `project`: identity, type, goals, stage, roles
- `deliverables`: what must be produced and how completion is measured
- `documents_required`: mandatory artifacts to create/maintain
- `context_modules`: reusable policy and execution libraries
- `workflows`: stage gates and QC checks
- `agents`: bot responsibilities and boundaries
- `airtable`: mapping of PCP entities to Airtable tables/fields

## Quick Start

1. Copy an example from `examples/`.
2. Validate your PCP file against `schema/pcp.schema.json`.
3. Reference reusable defaults from `library/`.
4. Map entities into Airtable using `airtable/field-mapping.md`.

## Repository Layout

- `SPECIFICATION.md`: protocol specification
- `schema/pcp.schema.json`: JSON Schema for PCP payloads
- `examples/`: complete sample PCP payloads
- `library/`: reusable project types, deliverables, docs, context modules
- `airtable/`: Airtable integration guidance
- `templates/`: document templates used by PCP payloads
- `docs/`: operational templates and reference docs
- `WindCalculations/`: standardized wind-calculation subcategory playbooks


## New: Standardized Engineering Intake Matrix

For teams mapping project types to default deliverables, required documents, and execution resources:

- Canonical matrix: `library/taxonomy/project-delivery-matrix.json`
- Operational guidance: `docs/standardized-sop-framework.md`
- Example generated PCP payload: `examples/container-home-pcp.json`

This gives you a machine-readable baseline for Airtable automations and bot task assignment.

Wind subcategory playbooks are available under `WindCalculations/` and mapped in `library/taxonomy/project-delivery-matrix.json`.


## New: Standardized Engineering Intake Matrix

For teams mapping project types to default deliverables, required documents, and execution resources:

- Canonical matrix: `library/taxonomy/project-delivery-matrix.json`
- Operational guidance: `docs/standardized-sop-framework.md`
- Example generated PCP payload: `examples/container-home-pcp.json`

This gives you a machine-readable baseline for Airtable automations and bot task assignment.

## Versioning

Protocol versioning uses semantic versioning in `pcp_version`.

- Major: breaking structural changes
- Minor: backward-compatible additions
- Patch: clarifications and non-breaking fixes

## Open Source Intent

This repository is designed as a shared public baseline for teams and autonomous systems. You can fork it, extend it, and propose upstream improvements.
