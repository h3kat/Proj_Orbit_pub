# Contributing to Project ORBIT

Thank you for your interest in Project ORBIT.

ORBIT is an early-stage research project. Contributions are welcome, but the public repository intentionally separates public collaboration from restricted mechanisms and experiments.

## Read first

Before contributing, read:

- `README.md`
- `STATUS.md`
- `RESEARCH_CONTEXT.md`
- `DISCLOSURE_POLICY.md`
- `SECURITY.md`
- `NOTICE.md`

## High-value contributions

### Prior-art corrections

Useful examples include:

- a paper that invalidates an ORBIT assumption;
- an existing implementation that already solves something ORBIT planned to build;
- a stronger benchmark;
- evidence that two apparently distinct mechanisms are equivalent.

Finding that ORBIT is wrong is a useful contribution.

### Reproducible evaluations

Especially useful:

- minimal failure cases;
- benchmark improvements;
- backend or model comparisons;
- reproducibility fixes;
- false-positive / false-blocking analysis;
- failure attribution.

### Thin infrastructure adapters

Adapters for runtimes, durable execution systems, model providers, tool protocols, observability, storage, sandboxing, and test harnesses can be useful. External frameworks should not define ORBIT's internal semantics.

### Documentation

Corrections to terminology, references, reproducibility instructions, limitations, trade-offs, and negative results are welcome.

## Do not post publicly

Do not open a public issue or pull request containing:

- undisclosed ORBIT core mechanisms;
- detailed bypasses of control boundaries;
- sensitive adversarial cases;
- methods for unauthorized capability or authority escalation;
- private benchmark data;
- credentials or tokens;
- restricted collaborator material;
- exploit code covered by `SECURITY.md`.

Use the private security/contact channel instead.

## Research contribution standard

A feature proposal should answer at least one of these questions:

1. What measurable problem does it solve?
2. What existing system does it improve upon or replace?
3. How would we know if it fails?
4. Can the mechanism be swapped without changing the research claim?
5. Does it belong in ORBIT core, or should it be an adapter/dependency?

"Interesting" is not sufficient by itself.

## Reuse before implementation

Before proposing a new subsystem:

1. search the literature;
2. search maintained open-source implementations;
3. check licensing and usage constraints;
4. determine whether an adapter is sufficient;
5. implement only what remains necessary.

> **Do not build infrastructure merely to make ORBIT larger.**

If another project solves the problem better, reuse it.

## Evidence and claims

Keep these distinct where relevant:

- observation;
- hypothesis;
- implementation;
- experiment;
- evidence;
- conclusion.

Do not silently promote a plausible idea into a validated result, a demo into a general claim, model confidence into evidence, or a citation into proof that ORBIT itself works.

## Pull requests

Prefer small, reviewable PRs. For behavior-changing work, include tests and dependency/license impact where applicable.

A useful PR description can include:

```text
Problem:
Existing behavior:
Proposed change:
Expected measurable effect:
Failure condition:
Dependencies:
Disclosure impact:
```

## Dependencies

New dependencies should document:

- project/repository;
- version or commit when practical;
- license;
- role in ORBIT;
- whether modified;
- whether runtime, development, benchmark, or reference-only;
- known special restrictions.

A public repository with no clear license should not be copied into ORBIT code merely because it is publicly readable.

## AI-assisted contributions

AI-assisted code and documentation are allowed, but the contributor remains responsible for correctness, licensing, provenance, security, tests, accidental third-party code inclusion, and accidental disclosure of restricted material.

Model output is not authoritative merely because it is confident.

## Disclosure review

Before publishing a contribution, ask:

> **Does this create more verification value than operational leverage?**

If unclear and the change touches autonomy, persistence, capability acquisition, authority, recovery, self-modification, or security boundaries, use restricted review rather than publishing the sensitive mechanism by default.

## Conduct

Technical disagreement is expected. Attack assumptions, not people. Cite prior work. Preserve uncertainty. Update positions when evidence changes.

A contribution that removes an unnecessary ORBIT subsystem may be more valuable than one that adds a new subsystem.

## Current priority order

1. falsifiable hypothesis;
2. benchmark;
3. minimal prototype;
4. adversarial evaluation;
5. cross-backend replication;
6. only then broader capability expansion.

## Licensing note

This repository does not currently grant a general open-source license to original ORBIT material unless a specific file or directory explicitly states otherwise. Contributors should not submit material they do not have the right to contribute.

---

**Project ORBIT**

*Convergence is information. Prior art is compressed research time.*

*The goal is not to own the answer. The goal is to shorten the path to the answer.*
