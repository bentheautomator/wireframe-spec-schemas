# wireframe-spec schemas

Public JSON Schema definitions for [bentheautomator/wireframe-spec][source].

Mirror of `<source>/schemas/`. Updated via `scripts/sync-schemas.sh` in the source repo on every schema change.

## Files

| File | Describes |
|---|---|
| `spec.json` | Top-level `wireframe-spec extract` output (scenes + nested sidecar blocks). |
| `project-manifest.json` | `wireframe-spec init` output / project configuration. |
| `design.schema.json` | `design.md` sidecar (parsed by `wireframe-spec extract`). |
| `specs.schema.json` | `specs.md` sidecar — endpoints, models, elements. |
| `policy.schema.json` | `policy.md` sidecar — principals, roles, rules, audit events. |
| `tests.schema.json` | `tests.md` sidecar — test cases, coverage rows. |

## Usage

```bash
# Validate a spec.json:
check-jsonschema \
  --schemafile https://raw.githubusercontent.com/bentheautomator/wireframe-spec-schemas/main/spec.json \
  path/to/spec.json
```

[source]: https://github.com/bentheautomator/wireframe-spec
