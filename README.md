# ARCHICUSTOS

Primitive ID: PRIM-002  
Package: @verifrax/archicustos  
Binary: archicustos

Verifrax primitive — custody preservation primitive for deterministic irreversible systems.

---

## Status

Current release status: pre-stable primitive release line.

Canonical release target:

package version: 0.1.0  
tag: v0.1.0

ARCHICUSTOS is part of the Verifrax primitive layer and follows the canonical primitive governance, naming, version, and packaging rules.

---

## Purpose

ARCHICUSTOS preserves deterministic custody after origin has been fixed.

Once an artifact has a stable origin, custody must remain legible, bounded, and preservable across handling events. ARCHICUSTOS exists to keep that custody surface from becoming ambiguous, discontinuous, or silently drifting over time.

It does not establish origin. It does not verify truth. It does not witness, judge, or terminate. Its role is narrower: preserve custody continuity after origin exists.

---

## What This Primitive Does

- preserves custody continuity for an already-originated artifact
- records or enforces a stable custody-preservation surface
- emits custody-bound output suitable for downstream primitives

---

## What This Primitive Does Not Do

- does not establish first origin
- does not determine temporal ordering beyond custody-preservation context
- does not verify correctness
- does not witness or attest
- does not judge validity
- does not terminate lifecycle

---

## Behavioral Contract

Invocation model:

executable: archicustos  
package: @verifrax/archicustos  
runtime: CLI-first

The primitive operates on an artifact whose origin surface is already fixed.

If origin is absent, custody preservation is undefined. ARCHICUSTOS must not fabricate prior origin or pretend custody continuity exists where no stable origin anchor exists.

Exit codes:

0 — custody preservation completed successfully  
non-zero — invocation failed or contract violated

---

## Usage

Install:

npm install -g @verifrax/archicustos

Execute:

archicustos artifact.json

stdin example:

cat artifact.json | archicustos

---

## Determinism Guarantees

For identical canonical input, ARCHICUSTOS must produce identical custody-preservation output.

No hidden environmental state may influence the result.

ARCHICUSTOS assumes an already-bounded origin surface and does not substitute for origin fixation, verification, or later judgment primitives.

---

## Security Model

ARCHICUSTOS protects against ambiguity or silent drift in custody continuity.

Its security value is to preserve legible custody after origin. It does not guarantee validity, attestation, or irreversible judgment, and it must not be described as a substitute for those downstream roles.

---

## Relationship to Other Primitives

Canonical primitive order:

1 originseal  
2 archicustos  
3 kairoclasp  
4 limenward  
5 validexor  
6 attestorium  
7 irrevocull  
8 guillotine

Repositories:

https://github.com/Verifrax/originseal  
https://github.com/Verifrax/archicustos  
https://github.com/Verifrax/kairoclasp  
https://github.com/Verifrax/limenward  
https://github.com/Verifrax/validexor  
https://github.com/Verifrax/attestorium  
https://github.com/Verifrax/irrevocull  
https://github.com/Verifrax/guillotine

---

## Installation

npm install -g @verifrax/archicustos

command -v archicustos

Repository:
- GitHub: https://github.com/Verifrax/archicustos
- Package: @verifrax/archicustos
- Binary: archicustos

---

## License

MIT
