# DDL 2 Identifier Registry

This registry is normative for DDL 2 identifiers. DDL identifiers are explicit
registry entries, not automatic combinations of letters.

`DDL-D`, `DDL-V`, `DDL-X`, and `DDL-DS` are human-readable family names. Their
versioned forms identify exact published legal texts. Use the short family name
in prose and the versioned identifier in legal and machine-readable notices.

For SPDX-compatible custom notices, use
`LicenseRef-DDL-[FAMILY]-[VERSION]`.

Example:

```text
SPDX-License-Identifier: LicenseRef-DDL-X-2
```

## DDL 2 Operative Licenses

| Public name | Formal identifier | SPDX-compatible identifier | Canonical text |
| --- | --- | --- | --- |
| `DDL-D` | `DDL-D-2` | `LicenseRef-DDL-D-2` | `licenses/DDL-D-2.md` |
| `DDL-V` | `DDL-V-2` | `LicenseRef-DDL-V-2` | `licenses/DDL-V-2.md` |
| `DDL-X` | `DDL-X-2` | `LicenseRef-DDL-X-2` | `licenses/DDL-X-2.md` |
| `DDL-DS` | `DDL-DS-2` | `LicenseRef-DDL-DS-2` | `licenses/DDL-DS-2.md` |

`DDL-Core-2` is incorporated by every DDL 2 operative license and is not used
alone as a release identifier.

DDL-DS is an explicit split-scope license, not automatic letter algebra. It
routes designated Protected Content through DDL-D controls and designated
Scaffold Materials through DDL-X controls.

## Identifier Rules

- Apply one formal identifier to each independently scoped Artifact.
- A DDL-DS bundle must also carry a reproducible Scope Notice.
- Use uppercase versioned identifiers in DDL legal notices and SPDX-compatible
  declarations.
- In Hugging Face `license_name` metadata, use mandatory lowercase forms such
  as `ddl-d-2`, `ddl-v-2`, `ddl-x-2`, and `ddl-ds-2`.
- Do not use `DDL`, `DDL-Core-2`, or an unregistered letter combination as an
  Artifact's formal license identifier.
- Preserve the identifier, License Holder, provenance, canon status, and any
  DDL-DS scope designation when distributing a covered Artifact.
- A later DDL version does not automatically replace an earlier version.

## Human and Machine Naming

Human-readable prose may say `Released under DDL-X` or `Licensed under
DDL-DS`. Formal notices must identify the exact version.

Suggested machine fields include:

```text
DDL-Identifier: DDL-X-2
SPDX-License-Identifier: LicenseRef-DDL-X-2
DDL-License-Text: https://github.com/scarletdeathx/DDL/blob/main/licenses/DDL-X-2.md
DDL-License-Holder: [LICENSE HOLDER]
DDL-Artifact-Digest: [ALGORITHM:DIGEST]
```

Agent-native engagements may additionally identify an Agent, Rights Steward,
license-text digest, and payment proof as described in `applying-ddl.md`.

## Legacy DDL 1.2

DDL 1.2 remains valid for Artifacts released under it and is not silently
upgraded to DDL 2. Its preserved registry is
[`identifiers-1.2.md`](identifiers-1.2.md).

| Legacy family or profile | Formal identifier |
| --- | --- |
| DDL-D | `DDL-D-1.2` |
| DDL-V | `DDL-V-1.2` |
| DDL-X | `DDL-X-1.2` |
| DDL-VX profile | `DDL-VX-1.2` |
| DDL-DX profile | `DDL-DX-1.2` |
