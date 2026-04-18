# DDL 1.2 Identifier Registry

This registry is normative for DDL 1.2 identifiers. DDL profiles are explicit
registry entries, not automatic combinations of letters.

`DDL-D`, `DDL-V`, and `DDL-X` are the human-readable family names. The
versioned forms such as `DDL-V-1.2` identify a specific published legal text.
Use the family names in prose and public-facing descriptions. Use the versioned
identifiers in legal notices, machine-readable declarations, and other places
where exact legal text matters.

For machine-readable notices, use SPDX-compatible custom identifiers in the
form `LicenseRef-DDL-[IDENTIFIER]`.

Example:

```text
SPDX-License-Identifier: LicenseRef-DDL-X-1.2
```

## Operative Licenses

| Human identifier | SPDX-compatible identifier | Canonical text |
| --- | --- | --- |
| `DDL-D` | `LicenseRef-DDL-D-1.2` | `licenses/DDL-D-1.2.md` |
| `DDL-V` | `LicenseRef-DDL-V-1.2` | `licenses/DDL-V-1.2.md` |
| `DDL-X` | `LicenseRef-DDL-X-1.2` | `licenses/DDL-X-1.2.md` |

`DDL-Core-1.2` is incorporated by each operative license. It is not used alone
as a license identifier for released artifacts.

## Profiles

| Profile | SPDX-compatible identifier | Expansion |
| --- | --- | --- |
| `DDL-VX-1.2` | `LicenseRef-DDL-VX-1.2` | Canon-origin gift into DDL-X lineage. Downstream artifacts inherit `DDL-X-1.2`, preserve provenance, and remain Non-Canon unless elevated. |
| `DDL-DX-1.2` | `LicenseRef-DDL-DX-1.2` | Callable or inference-only protected artifact. No copying, redistribution, modification, extraction, training, or dataset reconstruction. |

Most releases should use the three operative license families directly. For
DDL 1.2, only `DDL-VX-1.2` and `DDL-DX-1.2` remain as registered special-case
profiles.

## Identifier Rules

- Use exactly one operative license identifier or one registered profile
  identifier for a released artifact.
- In prose and public-facing descriptions, `DDL-D`, `DDL-V`, and `DDL-X` may
  be used as shorthand for the current family.
- In `LICENSE`, formal legal notices, SPDX-style declarations, and other
  machine-readable metadata, use the full versioned identifier such as
  `DDL-V-1.2`.
- Do not invent combined identifiers outside this registry for DDL 1.2.
- Do not use `DDL` by itself as a license identifier.
- Do not use `DDL-Core-1.2` by itself as a license identifier.
- Preserve the DDL identifier, license holder, provenance notice, and
  canon-status notice when distributing a DDL artifact.
