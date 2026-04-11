# deathOS Distributed License (DDL) 1.2

DDL is a modular license specification for canon-aware generative works:
protected source material, canon-origin models, and community model lineages.

This repository publishes the DDL 1.2 license family and its identifier
registry. It is a draft framework and is not legal advice.

## Operative Licenses

DDL has three operative license families:

| Identifier | Use for | Canon posture |
| --- | --- | --- |
| `DDL-D-1.2` | Protected source material and Canon Datasets | Closed, personal access only |
| `DDL-V-1.2` | Canon-origin model releases | Derivatives are Non-Canon unless elevated |
| `DDL-X-1.2` | Community releases and downstream lineage | Non-Canon, inheriting DDL-X |

Canonical texts:

- [DDL-Core-1.2](licenses/DDL-Core-1.2.md)
- [DDL-D-1.2](licenses/DDL-D-1.2.md)
- [DDL-V-1.2](licenses/DDL-V-1.2.md)
- [DDL-X-1.2](licenses/DDL-X-1.2.md)

## Profiles

Profiles such as `DDL-VX-1.2` are registered release postures. They are not
automatic letter algebra. Each profile expands to an operative DDL license and
states how provenance, canon status, and inheritance should be read.

Use [identifiers.md](identifiers.md) as the normative registry for all DDL
identifiers and profiles.

## Applying DDL

Use [applying-ddl.md](applying-ddl.md) for file notices, model card snippets,
dataset card snippets, and practical release guidance.

For Hugging Face releases, use the ready-to-copy templates in
[templates/huggingface](templates/huggingface/).

Typical choices:

- Use `DDL-D-1.2` for protected source datasets or canon source material that
  can be personally viewed but not trained on or redistributed.
- Use `DDL-V-1.2` for an official canon-origin model where commercial
  fine-tunes are allowed but downstream work is Non-Canon.
- Use `DDL-X-1.2` for community releases, downstream models, and datasets
  derived from DDL-X models or outputs.
- Use `DDL-VX-1.2` when a canon-origin release is intentionally gifted into
  DDL-X community lineage.

## Repository License

The repository prose and tooling are MIT-licensed unless a file states
otherwise. The DDL license texts and registry are published license artifacts;
see [NOTICE.md](NOTICE.md) for copying and attribution terms.
