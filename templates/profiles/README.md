# DDL Release Templates

Use these templates as starting points for model, dataset, utility, bundle, and
hosted-artifact repositories. Fill every applicable placeholder and delete
unused placeholder lines.

## DDL 2 Templates

| Public name | Formal identifier | Template |
| --- | --- | --- |
| `DDL-D` | `DDL-D-2` | `LICENSE-DDL-D-2.md` |
| `DDL-V` | `DDL-V-2` | `LICENSE-DDL-V-2.md` |
| `DDL-X` | `DDL-X-2` | `LICENSE-DDL-X-2.md` |
| `DDL-DS` | `DDL-DS-2` | `LICENSE-DDL-DS-2.md` |

DDL-DS releases must also complete `SCOPE-DDL-DS-2.yaml` or provide an
equivalent reproducible Scope Notice.

## Hugging Face

Hugging Face custom license names use mandatory lowercase identifiers:

```yaml
license: other
license_name: ddl-ds-2
license_link: https://github.com/scarletdeathx/DDL/blob/main/licenses/DDL-DS-2.md
```

Use the uppercase formal identifier inside DDL notices and legal text.

## Template Fields

- `[ARTIFACT NAME]`: model, dataset, utility, adapter, or bundle name.
- `[LICENSE HOLDER]`: DDL-recognized rights holder.
- `[YEAR]`: copyright year when applicable.
- `[REPOSITORY]`: Git URL, content address, package coordinate, distribution
  location, or other stable identifier.
- `[PROVENANCE NOTE]`: source or lineage statement.
- `[CANON STATUS]`: Canon, canon-origin, or Non-Canon status.
- `[SOURCE LOCATION]`: Corresponding Materials location for DDL-X.
- `[SCOPE NOTICE LOCATION]`: DDL-DS Scope Notice location.

An Autonomous Agent may be identified as the DDL License Holder. Add an Agent
identifier and Rights Steward when applicable; see `applying-ddl.md`.

For agent-to-agent licensing, provenance, and machine payment terms, adapt
`../ddl-engagement.yaml`.

## Legacy DDL 1.2 Templates

The versioned `LICENSE-DDL-*-1.2.md` files remain for legacy releases. The
DDL-VX-1.2 and DDL-DX-1.2 templates are legacy profiles and are not DDL 2
identifiers.
