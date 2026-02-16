# Container Plans Deliverable: Index of Sheets

This reference defines a standard permit-package sheet index for the `container-plans` deliverable.

## Suggested Codex package structure

```text
Container_Plans/
    index_of_sheets.md
    architectural/
        A0_Cover_Sheet.md
        A1_Site_Plan.md
        ...
    electrical/
        E0_Electrical_Notes.md
        ...
    mechanical/
        M1_Mech_Schedule.md
        ...
    plumbing/
        P1_Plumbing_Specs.md
        ...
    structural/
        S1_Foundation_Plan.md
        ...
```

## Sheet index

### Architectural Sheets

- A.0 — Cover Sheet
- A.1 — Site Plan
- A.2 — 1st Floor Plan
- A.3 — 2nd Floor Plan
- A.4 — Elevations
- A.5 — General Notes
- A.6 — Container Details (1)
- A.7 — Container Details (2)

### Electrical Sheets

- E.0 — Electrical Notes
- E.1 — 1st Floor Power Plan
- E.2 — 2nd Floor Power Plan
- E.3 — 1st Floor Lighting Plan
- E.4 — 2nd Floor Lighting Plan

### Mechanical Sheets

- M.1 — Mechanical Specs and Schedule
- M.2 — 1st Floor Mechanical Plan
- M.3 — 2nd Floor Mechanical Plan

### Plumbing Sheets

- P.1 — Plumbing Specs
- P.2 — Details and Notes
- P.3 — 1st Floor Plumbing Water Plan
- P.4 — 2nd Floor Plumbing Water Plan
- P.5 — 1st Floor Sanitary Plan
- P.6 — 2nd Floor Sanitary Plan
- P.7 — Plumbing Details

### Structural Sheets

- S.1 — Foundation Plan
- S.2 — 1st Floor Framing Plan
- S.3 — 2nd Floor Framing Plan
- S.4 — Roof Framing Plan
- S.5 — Foundation General Notes
- S.6 — Details & Connections (1)
- S.7 — Details & Connections (2)
- S.8 — Details & Connections (3)
- S.9 — Section (1)
- S.10 — Section (2)
- S.11 — 1st Floor Shear Wall Plan
- S.12 — 2nd Floor Shear Wall Plan
- S.13 — Typical Opening Details (1)
- S.14 — Typical Opening Details (2)

## Sheet metadata template

Use one record per sheet entry with fields similar to the following:

```yaml
sheet_id: "A.2"
title: "1st Floor Plan"
discipline: "Architectural"
description: "Floor plan showing layout of the first floor, doors, openings, and key dimensions."
required_inputs:
  - "Site survey"
  - "Owner layout approval"
calculation_refs:
  - "templates/calculations/load-path-template.md"
clients_expected_outputs:
  - "Permit-ready PDF sheet"
  - "DWG source file"
dependencies:
  - "Site Plan"
  - "Container Details"
deliverable: "Container Plans"
```

### Suggested metadata fields

| Field | Purpose |
| --- | --- |
| `sheet_id` | Unique code (A.0, S.1, etc.). |
| `title` | Human-readable sheet title. |
| `discipline` | Architectural, Structural, Mechanical, Electrical, or Plumbing. |
| `description` | Short summary of sheet scope. |
| `required_inputs` | Files/data needed to produce the sheet. |
| `calculation_refs` | Links to scripts, templates, or calculation packages. |
| `clients_expected_outputs` | Permit-set outputs expected by client/reviewer. |
| `dependencies` | Related sheets/documents referenced by this sheet. |
