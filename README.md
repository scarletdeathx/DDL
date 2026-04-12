# deathOS Distributed License (DDL) 1.2

DDL is a modular license specification for canon-aware generative works:
protected source material, canon-origin models, and community model lineages.

This repository publishes the DDL 1.2 license family and its identifier
registry. It is a draft framework and is not legal advice.

## Operative Licenses

DDL has three operative license families:

| Identifier | Use for | Canon posture |
| --- | --- | --- |
| `DDL-D` | Protected source material and Canon Datasets | Closed, personal access only |
| `DDL-V` | Canon-origin model releases | Derivatives are Non-Canon unless elevated |
| `DDL-X` | Community releases and downstream lineage | Non-Canon, inheriting DDL-X |

Canonical texts:

- [DDL-Core-1.2](licenses/DDL-Core-1.2.md)
- [DDL-D-1.2](licenses/DDL-D-1.2.md)
- [DDL-V-1.2](licenses/DDL-V-1.2.md)
- [DDL-X-1.2](licenses/DDL-X-1.2.md)

## Naming And Versioning

`DDL-D`, `DDL-V`, and `DDL-X` are the human-readable names of the DDL license
families. Use them in prose, badges, release descriptions, and other public-
facing contexts.

`DDL-D-1.2`, `DDL-V-1.2`, and `DDL-X-1.2` identify the exact published legal
texts. Use the versioned identifiers in `LICENSE`, formal legal notices,
SPDX-style declarations, and other places where the legal text must be exact.

Repository commits do not change the DDL version number. Only deliberate
changes to the operative license text, definitions, permissions, restrictions,
inheritance rules, or profile meanings should produce a new DDL version.

## Profiles

Profiles such as `DDL-VX-1.2` are registered release postures. They are not
automatic letter algebra. Each profile expands to an operative DDL license and
states how provenance, canon status, and inheritance should be read.

Use [identifiers.md](identifiers.md) as the normative registry for all DDL
identifiers and profiles.

## Applying DDL

Use [applying-ddl.md](applying-ddl.md) for file notices, model card snippets,
dataset card snippets, and practical release guidance.

For release repositories, use the ready-to-copy templates in
[templates/profiles](templates/profiles/).

Typical choices:

- Use `DDL-D` for protected source datasets or canon source material that
  can be personally viewed but not trained on or redistributed.
- Use `DDL-V` for an official canon-origin upstream model where commercial
  fine-tunes and downstream releases are allowed, but downstream work remains
  Non-Canon unless elevated.
- Use `DDL-X` for community releases, downstream models, and datasets
  derived from DDL-X models or outputs.
- Use `DDL-VX` when a canon-origin release is intentionally gifted into
  DDL-X community lineage.

## Reading DDL-V

`DDL-V` is the permissive canon-origin lane in the DDL family. It is meant for
an official-origin model release that others may use, fine-tune, commercialize,
and build on without receiving official affiliation or canon status.

Under `DDL-V`, downstream outputs, derivative models, derivative datasets, and
output collections are Non-Canon by default unless the License Holder
explicitly elevates them. `DDL-V` does not automatically convert downstream
material into `DDL-D`, and it does not automatically force `DDL-X`
inheritance.

Instead, `DDL-V` preserves provenance and canon-boundary restrictions while
leaving downstream creators free to choose how to release the rights they
actually hold in their own downstream material, subject to applicable law and
the Canon Dataset protections in `DDL-V-1.2`.

## Repository License

The repository prose and tooling are MIT-licensed unless a file states
otherwise. The DDL license texts and registry are published license artifacts;
see [NOTICE.md](NOTICE.md) for copying and attribution terms.
