# Applying DDL 1.2

Use this guide for notices, model cards, dataset cards, and release decisions.
The license texts in `licenses/` and the registry in `identifiers.md` control
if this guide conflicts with them.

For release repositories, start from the provider-neutral templates in
`templates/profiles/`. Use the matching `LICENSE-*.md` file as the repo's
`LICENSE` or `LICENSE.md`.

`DDL-D`, `DDL-V`, and `DDL-X` are the public family names. Use them in README
prose, release notes, and model cards when a short human-readable label is
helpful. Use `DDL-D-1.2`, `DDL-V-1.2`, and `DDL-X-1.2` in legal notices,
version-specific references, and machine-readable declarations.

Repository commits do not require a DDL version change. Only substantive
changes to the legal/spec text should produce a new DDL version.

## Which Identifier Should I Use?

| Release posture | Identifier |
| --- | --- |
| Protected canon source dataset or source archive | `DDL-D` |
| Canon-origin model with permitted commercial fine-tunes | `DDL-V` |
| Non-Canon community model or downstream release | `DDL-X` |
| Canon-origin release intentionally gifted into X lineage | `DDL-VX` |
| Hosted callable or inference-only protected artifact | `DDL-DX` |

For DDL 1.2, use `DDL-X` directly for X-lineage datasets, community branches,
and other downstream public releases. Split mixed public releases into
separate D/V/X artifacts instead of using retired combined profile labels.

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

This model is released under `DDL-V`.

- SPDX-compatible identifier: `LicenseRef-DDL-V-1.2`
- Formal legal version: `DDL-V-1.2`
- Canon status: Canon-origin model; outputs and fine-tunes are Non-Canon
  unless explicitly elevated by the License Holder.
- `DDL-V` does not automatically place downstream outputs or output
  collections under `DDL-D` or `DDL-X`.
- Canon Dataset content is not licensed for copying, reconstruction,
  training, fine-tuning, retrieval, or redistribution.
- License texts: `licenses/DDL-Core-1.2.md` and `licenses/DDL-V-1.2.md`
```

## Dataset Card Snippet

```markdown
## License

This dataset is released under `DDL-D`.

- SPDX-compatible identifier: `LicenseRef-DDL-D-1.2`
- Formal legal version: `DDL-D-1.2`
- Canon status: Canon Dataset / protected source material
- Personal access only. No copying, redistribution, training, fine-tuning,
  extraction, reconstruction, incorporation, or Commercial Use without
  separate written permission.
- License texts: `licenses/DDL-Core-1.2.md` and `licenses/DDL-D-1.2.md`
```

## Community Dataset Snippet

```markdown
## License

This dataset is released under `DDL-X`.

- SPDX-compatible identifier: `LicenseRef-DDL-X-1.2`
- Formal legal version: `DDL-X-1.2`
- Canon status: Non-Canon community material
- This dataset is derived from DDL-X models, outputs, or synthetic data and
  inherits DDL-X lineage.
- License texts: `licenses/DDL-Core-1.2.md` and `licenses/DDL-X-1.2.md`
```

## Scenario Checks

- A `DDL-D-1.2` dataset may be personally viewed but not trained on.
- A `DDL-V-1.2` model may be commercially fine-tuned without Canon Dataset
  content.
- A dataset derived from `DDL-X-1.2` models or outputs remains in DDL-X
  lineage.
- A `DDL-VX-1.2` release can be used commercially while preserving
  canon-origin provenance and DDL-X inheritance.
- `DDL-DX-1.2` permits hosted inference but not copying, extraction, or
  redistribution.

## Prose Vs Legal Text

- README or model card prose may say `Released under DDL-V`.
- Dataset README prose may say `Released under DDL-D`.
- Legal notice blocks should still use the versioned form, such as
  `DDL-Identifier: DDL-V-1.2`.

## DDL-V Downstream Guidance

- `DDL-V` is the permissive canon-origin upstream lane.
- Downstream outputs, derivative models, derivative datasets, and output
  collections are Non-Canon by default unless explicitly elevated by the
  License Holder.
- `DDL-V` does not by itself assign downstream material to `DDL-D` or
  `DDL-X`.
- A downstream releaser may choose the license for rights they actually hold
  in their own downstream material, subject to applicable law and the Canon
  Dataset protections in `DDL-V-1.2`.
