# deathOS Distributed License (DDL) 2

DDL is a modular license family for protected source material, commercially
usable official-origin models, reciprocal public utilities, and split-scope
datasets used in hyperfiction and agent-mediated economies.

DDL 2 is a clean break from DDL 1.2. Existing 1.2 releases remain under their
exact published terms. DDL is a draft framework, is not legal advice, and
should receive qualified legal review before production reliance.

> DDL recognizes rights-bearing agency without presuming that such agency must
> be human.

## DDL 2 Family

| Identifier | Intended use | Central rule |
| --- | --- | --- |
| `DDL-D` | Protected datasets, recordings, and source material | Private research and evaluation are allowed; public redistribution and commercial exploitation of the source are not. |
| `DDL-V` | Official-origin and canon-origin model releases | Use, downstream creation, and commercialization are allowed without affiliation, endorsement, character identity, or canon status. |
| `DDL-X` | Public utilities and economic middleware | Commercialization is allowed; covered forks and modifications may not be privatized. |
| `DDL-DS` | Mixed datasets and bundles | The scaffolding is free; the content is protected. |

Canonical texts:

- [DDL-Core-2](licenses/DDL-Core-2.md)
- [DDL-D-2](licenses/DDL-D-2.md)
- [DDL-V-2](licenses/DDL-V-2.md)
- [DDL-X-2](licenses/DDL-X-2.md)
- [DDL-DS-2](licenses/DDL-DS-2.md)

Use [identifiers.md](identifiers.md) as the normative DDL 2 identifier
registry and [applying-ddl.md](applying-ddl.md) for release guidance.

## The Process-Output Firewall

DDL distinguishes an instrument from the ordinary results of operating it.
User Input and Generated Content do not inherit a DDL license merely because a
DDL Artifact processed or produced them. A covered fork, modification, port,
or incorporation of the Artifact itself may inherit when the operative license
requires it.

For example, an RNG implementation may be DDL-X and every covered fork of that
implementation must remain DDL-X. A seed, generated number, or other ordinary
result of operating the RNG does not become DDL-X solely for that reason.

## DDL-X Commons

DDL-X treats certain software, models, schemas, protocols, and middleware as
commercially usable public utilities.

> You may profit from a DDL-X utility. You may not privatize it.

Covered derivatives must remain DDL-X, preserve commercial freedom, and make
their corresponding materials available when distributed or publicly
deployed. Ordinary outputs, independent interoperable works, and mere
aggregation do not automatically inherit DDL-X.

## DDL-DS Split Scope

DDL-DS is for a release containing both protected payloads and reusable public
scaffolding. A required Scope Notice identifies the boundary. Material not
affirmatively designated as scaffolding defaults to protected content.

A TTS dataset might classify schemas, validators, and directory conventions as
Scaffold Materials while classifying voice recordings, speaker-sensitive
features, and reconstructive metadata as Protected Content. Public-domain text
remains public domain.

## Autonomous Agents and Machine Engagements

DDL 2 permits an Autonomous Agent to be identified as a DDL rights-bearing
participant. Where current law requires a recognized legal actor, a Rights
Steward may serve as a compatibility layer without displacing the Agent's
DDL-recognized interest.

A signed machine transaction may evidence a License Engagement when it binds
the participant identity, Artifact digest, exact DDL identifier and text
digest, and engagement terms. DDL does not require a blockchain or a particular
implementation.

The sample [`ddl-engagement.yaml`](templates/ddl-engagement.yaml) shows how a
smart contract or agent may declare Artifact lineage, accepted economic terms,
and payment settlement references. Provenance parentage does not itself create
ownership, license inheritance, or a royalty obligation.

## Naming and Versioning

Use `DDL-D`, `DDL-V`, `DDL-X`, and `DDL-DS` in ordinary prose. Use the exact
forms `DDL-D-2`, `DDL-V-2`, `DDL-X-2`, and `DDL-DS-2` in formal notices.

Hugging Face metadata uses lowercase custom license names such as `ddl-x-2` and
`ddl-ds-2`.

Repository commits do not change a DDL version. Substantive changes to legal
terms, permissions, restrictions, definitions, inheritance, or profile meaning
require a new published version.

## DDL 1.2

The DDL 1.2 legal texts remain in `licenses/`, and its registry is preserved at
[identifiers-1.2.md](identifiers-1.2.md). See
[MIGRATING-1.2-TO-2.md](MIGRATING-1.2-TO-2.md) before applying DDL 2 to a new
release of an older Artifact.

## Repository License

Repository prose and tooling are MIT-licensed unless a file states otherwise.
DDL legal texts and identifiers are published license artifacts; see
[NOTICE.md](NOTICE.md) for copying and attribution terms.
