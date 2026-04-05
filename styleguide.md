# DDL Styleguide

DDL is a modular licensing system. Each file or directory may declare one or
more DDL variants to indicate how it must be handled. Only the variants
(DDL‑D, DDL‑V, DDL‑X) apply rights or restrictions. “DDL” alone refers to the
overall system.

## Variants
DDL‑D   Canon Dataset License (no copying, no training, no redistribution)
DDL‑V   Canon Model License (finetuning allowed, derivatives remain Non‑Canon)
DDL‑X   Non‑Canon Model License (open aftermarket)

## Combined Tags
Multiple variants may be combined to describe mixed‑content projects.

DDL‑VX   Contains Canon Model components but must be distributed as Non‑Canon.
DDL‑XD   Contains Non‑Canon Model components and Non‑Canon datasets.
DDL‑XVD  Contains a mixture of V and D assets; all distribution must follow X.
DDL‑DV   Canon Dataset + Canon Model (internal use only; no redistribution).
DDL‑VD   Same as DV; ordering indicates emphasis only (model‑first vs dataset‑first).
DDL‑DX   Canon‑origin, read‑only assets; callable/inference‑only, not modifiable.
DDL‑XV   Non‑Canon distribution of a Canon‑lineage model; forms its own independent branch canon but cannot claim or inherit official Canon.

## Usage
- Apply DDL‑D, DDL‑V, or DDL‑X only to files you own.
- Combined tags describe the handling rules for a project or directory.
- Upstream open‑source licenses remain intact and are not replaced by DDL.
- “DDL” alone is never used as a license; it refers to the framework.
