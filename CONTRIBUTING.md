# Contributing

## Principles

- Keep PCP machine-first and human-readable.
- Prefer additive, backward-compatible changes.
- Include examples for every schema addition.

## Contribution Flow

1. Open an issue describing the change.
2. Update `schema/pcp.schema.json`.
3. Update `SPECIFICATION.md`.
4. Add or update examples under `examples/`.
5. Submit PR with migration notes if applicable.

## Compatibility

Any breaking shape changes must bump major version and include explicit migration guidance.
