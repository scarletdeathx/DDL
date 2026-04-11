# DDL 1.2 Identifier Registry

This registry is normative for DDL 1.2 identifiers. DDL profiles are explicit
registry entries, not automatic combinations of letters.

For machine-readable notices, use SPDX-compatible custom identifiers in the
form `LicenseRef-DDL-[IDENTIFIER]`.

Example:

```text
SPDX-License-Identifier: LicenseRef-DDL-X-1.2
```

## Operative Licenses

| Human identifier | SPDX-compatible identifier | Canonical text |
| --- | --- | --- |
| `DDL-D-1.2` | `LicenseRef-DDL-D-1.2` | `licenses/DDL-D-1.2.md` |
| `DDL-V-1.2` | `LicenseRef-DDL-V-1.2` | `licenses/DDL-V-1.2.md` |
| `DDL-X-1.2` | `LicenseRef-DDL-X-1.2` | `licenses/DDL-X-1.2.md` |

`DDL-Core-1.2` is incorporated by each operative license. It is not used alone
as a license identifier for released artifacts.

## Profiles

| Profile | SPDX-compatible identifier | Expansion |
| --- | --- | --- |
| `DDL-VX-1.2` | `LicenseRef-DDL-VX-1.2` | Canon-origin gift into DDL-X lineage. Downstream artifacts inherit `DDL-X-1.2`, preserve provenance, and remain Non-Canon unless elevated. |
| `DDL-XD-1.2` | `LicenseRef-DDL-XD-1.2` | X-lineage dataset or dataset/model bundle. Datasets derived from DDL-X models or DDL-X outputs inherit `DDL-X-1.2`. |
| `DDL-XVD-1.2` | `LicenseRef-DDL-XVD-1.2` | Mixed canon-origin and community bundle. Public distribution follows `DDL-X-1.2`; protected D source must be excluded or separately licensed under `DDL-D-1.2`. |
| `DDL-DV-1.2` | `LicenseRef-DDL-DV-1.2` | Internal protected Canon Dataset plus Canon Model bundle. No public redistribution. |
| `DDL-VD-1.2` | `LicenseRef-DDL-VD-1.2` | Same as `DDL-DV-1.2`; ordering indicates model-first editorial emphasis. |
| `DDL-DX-1.2` | `LicenseRef-DDL-DX-1.2` | Callable or inference-only protected artifact. No copying, redistribution, modification, extraction, training, or dataset reconstruction. |
| `DDL-XV-1.2` | `LicenseRef-DDL-XV-1.2` | Community branch lineage from a V or VX source. `DDL-X-1.2` applies; branch continuity may be named, but official canon status is not granted. |

## Identifier Rules

- Use exactly one operative license identifier or one registered profile
  identifier for a released artifact.
- Do not invent combined identifiers outside this registry for DDL 1.2.
- Do not use `DDL` by itself as a license identifier.
- Do not use `DDL-Core-1.2` by itself as a license identifier.
- Preserve the DDL identifier, license holder, provenance notice, and
  canon-status notice when distributing a DDL artifact.
