PRIM-007
ARCHICUSTOS
Custody primitive

STATUS: REGISTERED
REGISTRY: https://speedkit.eu
SNAPSHOT: https://speedkit.eu/REGISTRY_SNAPSHOT.json
```

Registered artifact. Identity governed by SPEEDKIT registry.

STATUS: FINAL

---

Registered artifact. Identity governed by SPEEDKIT registry.

STATUS: FINAL

---

**ARCHICUSTOS v0.0.0** is a custody primitive.

It does not decide.
It does not verify.
It does not witness.
It does not execute.
It does not enforce transitions.

It **guards custody**.

ARCHICUSTOS exists to make authority, responsibility, and ownership explicit across irreversible systems.

---

## Philosophy

Most failures are not technical.
They are failures of custody.

Who was responsible?
Who held authority?
Who had the right to act at that moment?

ARCHICUSTOS exists to prevent these questions from becoming unanswerable.

It answers one question only:

> **Who holds custody right now?**

Not who created.
Not who modified.
Not who claims.

Custody.

---

## What ARCHICUSTOS Is

ARCHICUSTOS is a **custody and authority primitive**.

It records and enforces continuity of custodianship over an artifact, system, or process.

It binds:

* Declared custodian (stdin)
* Repository identity
* Commit context
* Timestamp

Into a single, append-only custody ledger.

The result is **responsibility traceability**.

---

## What It Is Not

* Not an access control system
* Not an authentication mechanism
* Not a verifier
* Not a judge
* Not a workflow engine
* Not a governance framework

ARCHICUSTOS does not grant power.
It records **who already holds it**.

---

## Behavior

* Consumes custody declarations exclusively via `stdin`
* Refuses silent invocation
* Requires explicit custodian declaration
* Records custody claims immutably
* Enforces continuity (no orphaned custody)
* Emits exactly one verdict
* Exits immediately after recording

No retries.
No flags.
No configuration.

---

## Verdicts

ARCHICUSTOS emits exactly one of the following:

* `ACCEPTED` — custody recorded and continuous
* `DENIED` — custody invalid, ambiguous, or conflicting

The verdict concerns **authority continuity**, not correctness.

---

## Usage

ARCHICUSTOS is never run casually.
It is invoked when custody matters.

```sh
<custodian-identity> | ./archicustos.sh
```

### Example

```sh
echo "custodian: midiakiasat" | ./archicustos.sh
```

If custody is valid and continuous:

```text
ACCEPTED
```

If custody is invalid or breaks continuity:

```text
DENIED
```

---

## Contract

Once custody is recorded:

* Responsibility is explicit
* Authority is attributable
* Disputes become traceable
* Abdication is detectable

ARCHICUSTOS guarantees **no anonymous authority**.

---

## Relationship to Other Artifacts

* **GUILLOTINE** — executes
* **IRREVOCULL** — judges
* **ATTESTORIUM** — witnesses
* **VALIDEXOR** — verifies
* **LIMENWARD** — guards transitions
* **ORIGINSEAL** — seals origin
* **ARCHICUSTOS** — guards custody

Each artifact covers exactly one irreversible dimension.
None overlap.

---

## Warning

Custody creates liability.

If you invoke ARCHICUSTOS, you are declaring:

* "This is under my authority"
* "I accept responsibility"
* "I cannot later deny custody"

That is the point.

---

## About

ARCHICUSTOS is a minimal, deterministic custody primitive for irreversible systems.

If authority does not matter, do not use it.
If it does, nothing else is sufficient.

---

## Responsibility Boundary

This software is provided under the MIT License.

The MIT License permits use, copying, modification, and redistribution of the code, but it does not provide assurance, certification, audit defense, operational guarantees, or liability coverage.

Use of this software in environments where failure, compliance, legal exposure, or irreversible decisions matter requires an accountable party.

The original maintainer is available for assurance, adaptation, and responsibility when such accountability is required.

Contact: contact@speedkit.eu

Authoritative signed records are issued separately and are not produced by the software.
