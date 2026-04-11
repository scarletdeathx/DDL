# Applying DDL 1.2

Use this guide for notices, model cards, dataset cards, and release decisions.
The license texts in `licenses/` and the registry in `identifiers.md` control
if this guide conflicts with them.

For release repositories, start from the provider-neutral templates in
`templates/profiles/`. Use the matching `LICENSE-*.md` file as the repo's
`LICENSE` or `LICENSE.md`.

## Which Identifier Should I Use?

| Release posture | Identifier |
| --- | --- |
| Protected canon source dataset or source archive | `DDL-D-1.2` |
| Canon-origin model with permitted commercial fine-tunes | `DDL-V-1.2` |
| Non-Canon community model or downstream release | `DDL-X-1.2` |
| Canon-origin release intentionally gifted into X lineage | `DDL-VX-1.2` |
| Dataset derived from DDL-X models, outputs, or synthetic data | `DDL-XD-1.2` |
| Mixed V/X/D bundle prepared for public release | `DDL-XVD-1.2` |
| Internal protected canon dataset plus canon model bundle | `DDL-DV-1.2` or `DDL-VD-1.2` |
| Hosted callable or inference-only protected artifact | `DDL-DX-1.2` |
| Community branch lineage from a V or VX source | `DDL-XV-1.2` |

## Minimal Notice

```text
DDL-Identifier: DDL-X-1.2
SPDX-License-Identifier: LicenseRef-DDL-X-1.2
License-Text: https://example.com/licenses/DDL-X-1.2.md
License-Holder: [LICENSE HOLDER]
Canon-Status: Non-Canon
Provenance: Derived from [SOURCE ARTIFACT], if applicable.
```

For profiles, use the profile identifier in the first two lines and link to
both `identifiers.md` and the operative license text named by the profile.

## File Header Example

```text
Copyright (c) [YEAR] [LICENSE HOLDER]
DDL-Identifier: DDL-X-1.2
SPDX-License-Identifier: LicenseRef-DDL-X-1.2
Canon-Status: Non-Canon
```

## Model Card Snippet

```markdown
## License

This model is released under `DDL-V-1.2`.

- SPDX-compatible identifier: `LicenseRef-DDL-V-1.2`
- Canon status: Canon-origin model; outputs and fine-tunes are Non-Canon
  unless explicitly elevated by the License Holder.
- Canon Dataset content is not licensed for copying, reconstruction,
  training, fine-tuning, retrieval, or redistribution.
- License texts: `licenses/DDL-Core-1.2.md` and `licenses/DDL-V-1.2.md`
```

## Dataset Card Snippet

```markdown
## License

This dataset is released under `DDL-D-1.2`.

- SPDX-compatible identifier: `LicenseRef-DDL-D-1.2`
- Canon status: Canon Dataset / protected source material
- Personal access only. No copying, redistribution, training, fine-tuning,
  extraction, reconstruction, incorporation, or Commercial Use without
  separate written permission.
- License texts: `licenses/DDL-Core-1.2.md` and `licenses/DDL-D-1.2.md`
```

## Community Dataset Snippet

```markdown
## License

This dataset is released under `DDL-XD-1.2`.

- SPDX-compatible identifier: `LicenseRef-DDL-XD-1.2`
- Operative license: `DDL-X-1.2`
- Canon status: Non-Canon community material
- This dataset is derived from DDL-X models, outputs, or synthetic data and
  inherits DDL-X lineage.
- License texts: `identifiers.md`, `licenses/DDL-Core-1.2.md`, and
  `licenses/DDL-X-1.2.md`
```

## Scenario Checks

- A `DDL-D-1.2` dataset may be personally viewed but not trained on.
- A `DDL-V-1.2` model may be commercially fine-tuned without Canon Dataset
  content.
- A dataset derived from `DDL-X-1.2` models or outputs remains in DDL-X
  lineage.
- A `DDL-VX-1.2` release can be used commercially while preserving
  canon-origin provenance and DDL-X inheritance.
- `DDL-DV-1.2` and `DDL-VD-1.2` are internal-only protected bundles.
- `DDL-DX-1.2` permits hosted inference but not copying, extraction, or
  redistribution.
- `DDL-XV-1.2` may name community branch continuity but cannot claim official
  canon status.
