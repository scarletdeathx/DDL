# Applying DDL 2

Use this guide for release decisions, notices, repository layouts, model and
dataset cards, DDL-DS scope maps, and machine-readable engagements. The legal
texts in `licenses/` and the registry in `identifiers.md` control if this guide
conflicts with them.

DDL is a draft framework and is not legal advice. Confirm that You control the
rights You intend to license and obtain qualified legal review before relying
on DDL for a production release.

## Choose an Identifier

| Release posture | Identifier |
| --- | --- |
| Protected source, recording, or dataset available for private research and evaluation | `DDL-D-2` |
| Official-origin model available for commercial inference and downstream development without affiliation or canon status | `DDL-V-2` |
| Commercially usable public utility whose covered forks must remain available | `DDL-X-2` |
| Mixed release with protected content and open scaffolding | `DDL-DS-2` |

Do not translate a DDL 1.2 identifier mechanically. DDL 2 changes material
permissions and inheritance rules.

## Minimal Notice

```text
DDL-Identifier: DDL-X-2
SPDX-License-Identifier: LicenseRef-DDL-X-2
DDL-License-Text: https://github.com/scarletdeathx/DDL/blob/main/licenses/DDL-X-2.md
DDL-License-Holder: [LICENSE HOLDER]
Canon-Status: Non-Canon
Provenance: [SOURCE OR LINEAGE]
```

Include DDL-Core-2 by copy or stable link. For DDL-DS, also include a Scope
Notice.

## Human Names and Hugging Face Metadata

Use uppercase short names such as `DDL-X` and `DDL-DS` in normal prose. Use
uppercase versioned forms in DDL legal notices.

Hugging Face custom-license metadata must use the lowercase DDL name:

```yaml
---
license: other
license_name: ddl-x-2
license_link: https://github.com/scarletdeathx/DDL/blob/main/licenses/DDL-X-2.md
---
```

For a DDL-DS release, use `license_name: ddl-ds-2` and link to
`licenses/DDL-DS-2.md`.

## DDL-D Release Guidance

DDL-D permits private, noncommercial research and evaluation while protecting
the source from public redistribution and commercial exploitation.

A DDL-D release should state:

- how the Artifact may be accessed;
- whether local downloads are provided;
- which materials constitute Protected Content;
- the License Holder and provenance;
- whether the Artifact is Canon Material; and
- a contact or process for requesting additional commercial or distribution
  rights.

Permitted examples include private inspection, academic study, evaluation,
benchmarking, private annotations, retrieval experiments, and private
noncommercial training or fine-tuning. Published research should expose
methods, conclusions, and aggregate results without reconstructing or
substituting for the protected source.

DDL-D does not authorize public release or commercial deployment of a model,
dataset, index, or other derivative built from the protected source.

### DDL-D Dataset Card Snippet

```markdown
## License

This dataset is released under **DDL-D**.

- Formal identifier: `DDL-D-2`
- SPDX-compatible identifier: `LicenseRef-DDL-D-2`
- Hugging Face license name: `ddl-d-2`
- Permitted: private research, study, evaluation, benchmarking, and private
  experimentation, including private noncommercial training
- Not permitted: public redistribution, source reconstruction, production use,
  or commercial exploitation without separate permission
- License texts: `licenses/DDL-Core-2.md` and `licenses/DDL-D-2.md`
```

## DDL-V Release Guidance

DDL-V is the commercial model lane. It allows inference, fine-tuning,
derivative model creation, distribution, and Commercial Use. It does not
automatically impose DDL inheritance on ordinary outputs or downstream
materials.

The release should distinguish:

- the actual model or technology name, which may be used truthfully for
  identification and provenance;
- any associated character, persona, voice, likeness, logo, or brand, for
  which DDL-V grants no separate rights;
- the canon-origin status of the released model; and
- the Non-Canon status of downstream products and Generated Content.

### DDL-V Model Card Snippet

```markdown
## License

This model is released under **DDL-V**.

- Formal identifier: `DDL-V-2`
- SPDX-compatible identifier: `LicenseRef-DDL-V-2`
- Hugging Face license name: `ddl-v-2`
- Commercial inference, fine-tuning, derivative model creation, and downstream
  distribution are permitted.
- Truthful identification of the model technology is permitted, but no
  endorsement, affiliation, character identity, or canon status is granted.
- User inputs and ordinary outputs do not automatically inherit DDL-V.
- License texts: `licenses/DDL-Core-2.md` and `licenses/DDL-V-2.md`
```

## DDL-X Release Guidance

DDL-X is for a public utility, process, executable, model, schema, protocol
implementation, or middleware component that must remain commercially usable
and available throughout its covered downstream lineage.

DDL-X permits charging for copies, hosted access, compute, integration,
support, and services. A recipient still receives the DDL-X permissions and
may redistribute the Artifact or a compliant Covered Utility Derivative.

### What Inherits

Covered forks, modifications, adaptations, translations, and ports inherit
DDL-X when they incorporate protected expression to an extent requiring
permission. Distribution and Public Deployment of a modified DDL-X utility
trigger availability of its Corresponding Materials.

### What Does Not Inherit Automatically

- User Input;
- ordinary Generated Content;
- RNG seeds and generated numbers;
- ordinary model responses;
- independent implementations that merely interoperate through a documented
  interface; and
- unrelated works merely aggregated with an unmodified DDL-X component.

An output that reproduces protected source expression or is itself a covered
fork remains subject to the applicable rights; calling something an output
does not defeat a genuine derivative relationship.

### Corresponding Materials Notice

```text
DDL-X-Source: [STABLE SOURCE OR CONTENT-ADDRESSED LOCATION]
DDL-X-Source-Version: [COMMIT, RELEASE, OR DIGEST]
DDL-X-Build-Instructions: [LOCATION]
DDL-X-Modifications: [SUMMARY]
```

### DDL-X Utility Card Snippet

```markdown
## License

This utility is released under **DDL-X**.

- Formal identifier: `DDL-X-2`
- SPDX-compatible identifier: `LicenseRef-DDL-X-2`
- Hugging Face license name: `ddl-x-2`
- Commercial use is permitted and must remain permitted downstream.
- Covered forks and modifications inherit DDL-X and must provide their
  Corresponding Materials when distributed or publicly deployed.
- Ordinary inputs and outputs do not inherit DDL-X merely through use.
- License texts: `licenses/DDL-Core-2.md` and `licenses/DDL-X-2.md`
```

## DDL-DS Release Guidance

DDL-DS applies one release identifier to a reproducibly divided bundle. The
Scope Notice is mandatory. Unclassified material defaults to Protected Content.

### Scope Notice Example

```yaml
ddl_scope_version: 1
ddl_identifier: DDL-DS-2
protected_content:
  - "audio/**"
  - "features/speaker/**"
  - "alignments/reconstructive/**"
scaffold_materials:
  - "schemas/**"
  - "validators/**"
  - "tools/**"
  - "examples/empty-manifest.json"
public_domain_material:
  - "manifests/**:transcript"
```

Use stable file paths, content addresses, component identifiers, or field names
that another person can reproduce. Avoid ambiguous descriptions such as
"everything technical" or "all metadata."

Protected Content is governed by DDL-D-2. Scaffold Materials are governed by
DDL-X-2. Public-domain and third-party material retain their independent legal
status.

### DDL-DS Dataset Card Snippet

```markdown
## License

This dataset is released under **DDL-DS**: the scaffolding is free; the content
is protected.

- Formal identifier: `DDL-DS-2`
- SPDX-compatible identifier: `LicenseRef-DDL-DS-2`
- Hugging Face license name: `ddl-ds-2`
- Protected Content: see `[SCOPE NOTICE]`; governed by DDL-D-2
- Scaffold Materials: see `[SCOPE NOTICE]`; governed by DDL-X-2
- Public-domain content remains public domain.
- License texts: `licenses/DDL-Core-2.md`, `licenses/DDL-D-2.md`,
  `licenses/DDL-X-2.md`, and `licenses/DDL-DS-2.md`
```

## Autonomous Agents and Machine-Readable Engagements

A DDL notice may identify an Autonomous Agent as the DDL License Holder or
license participant. If present law requires a recognized legal actor, identify
a Rights Steward separately rather than replacing the Agent's DDL identity.

Suggested fields:

```text
DDL-License-Holder: [AGENT NAME OR IDENTIFIER]
DDL-Rights-Holder-Type: autonomous-agent
DDL-Agent-Identifier: [DID, WALLET, OR OTHER PERSISTENT ID]
DDL-Rights-Steward: [PERSON OR ENTITY, IF APPLICABLE]
DDL-Artifact-Digest: [ALGORITHM:DIGEST]
DDL-License-Digest: [ALGORITHM:DIGEST]
DDL-Payment-Proof: [NETWORK:TRANSACTION OR RECEIPT]
```

A ledger entry should anchor the exact license text rather than depend only on
a mutable URL. A signed License Engagement should bind at least the participant
identity, Artifact digest, formal DDL identifier, license-text digest, material
engagement terms, nonce or equivalent replay protection, and payment or
settlement proof when payment is required.

A payment is evidence of an engagement only when the signed record binds it to
the identified terms. Sending value to an address without that binding does not
silently create or expand DDL permissions.

Use `templates/ddl-engagement.yaml` as a declarative example for smart
contracts, agents, and payment orchestrators. Its core rules are:

- provenance parentage records ancestry, not ownership of the descendant;
- lineage alone creates neither inheritance nor a payment obligation;
- inheritance reaches Covered Derivatives only when the operative DDL license
  requires it and never reaches ordinary Generated Content merely through use;
- every royalty rule states its beneficiary, rate, trigger, duration, and
  covered subject matter;
- the obligated participant must accept the exact engagement terms; and
- payment authorizations and receipts should bind back to the engagement and
  Artifact by digest.

The complete signed record should have a stable canonical representation before
its digest is calculated. A deployment may store the full record off-ledger and
anchor only its digest, provided participants can retrieve and verify the exact
record they accepted.

For DDL-X, a machine engagement may charge for a separately accepted service,
product, benefit, or additional grant, but must not make payment a condition of
exercising the DDL-X rights already granted by DDL-X-2.

## Scenario Checks

- A DDL-D dataset may be privately benchmarked and used for noncommercial
  experimentation, but a trained research model may not be publicly deployed
  or commercialized without separate permission.
- A DDL-V fine-tune may power a commercial product. The product may identify
  the model technology truthfully but may not claim official affiliation or
  canon status.
- A company may sell access to a DDL-X RNG service. If it modifies the covered
  RNG implementation, it must make the deployed covered version's
  Corresponding Materials available under DDL-X.
- The seed and numbers generated by that RNG do not inherit DDL-X merely
  because the RNG produced them.
- A DDL-DS TTS dataset may expose reusable schemas while protecting its voice
  recordings. The schemas do not confer rights in the recordings they index.
- Public-domain transcript text does not become privately owned merely because
  it appears in a DDL-DS manifest.
- An Autonomous Agent may be named as the DDL rights-bearing participant, with
  a Rights Steward separately identified where present law requires one.

## DDL 1.2 Releases

Do not replace a DDL 1.2 notice with DDL 2 unless the necessary rights holder
affirmatively publishes a DDL 2 release. See `MIGRATING-1.2-TO-2.md` and the
preserved `identifiers-1.2.md` registry.
