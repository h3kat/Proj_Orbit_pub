# Disclosure Policy

## Purpose

Project ORBIT explores persistent and increasingly autonomous AI systems.

Some research in this area can improve reliability, auditability, and control.
The same implementation details may also reduce the effort required to construct systems
with stronger persistence, autonomy, capability acquisition, or resistance to external
intervention.

For that reason, Project ORBIT uses **staged disclosure**.

The objective is not secrecy for its own sake.

The objective is to publish enough information for meaningful technical evaluation and
collaboration **without unnecessarily lowering the cost of misuse before the relevant
mechanisms are adequately understood**.

---

## Disclosure principles

Project ORBIT follows five default principles.

### 1. Evidence should be easier to publish than operational leverage

Whenever possible, the project prefers to publish:

- the problem being studied;
- the hypothesis;
- the evaluation method;
- falsification criteria;
- aggregate results;
- known limitations;
- relevant prior work.

Operational details may be withheld when they add little independent scientific value
but substantially increase the ability to reproduce a risky mechanism.

### 2. Public descriptions should not imply validation

A mechanism being discussed does not mean it works.

A design being implemented does not mean it is safe.

A benchmark result does not automatically generalize beyond the tested conditions.

Project ORBIT therefore distinguishes between:

- proposal;
- implementation;
- experiment;
- evidence;
- validated result.

### 3. Capability growth does not imply authority growth

Research involving capability acquisition, tool use, persistent operation, or
self-modification should not be interpreted as support for unrestricted autonomy.

Where possible, capability and authority are treated as separate concerns.

### 4. Stronger autonomy requires stronger evaluation

As a mechanism becomes more persistent, autonomous, or operationally capable, the burden
of testing increases.

Publication decisions may therefore become more restrictive as the demonstrated
capability of a mechanism increases.

### 5. Disclosure decisions are revisable

Information may move from private to restricted, or from restricted to public, when:

- the mechanism becomes well understood;
- risks are reduced;
- equivalent information is already broadly available;
- publication has clear research value;
- external review supports broader disclosure.

Information may also be removed from planned publication if testing reveals previously unknown risks.

---

## Disclosure levels

### Level 0 — Public

Material appropriate for the public repository.

Examples:

- project motivation;
- research questions;
- high-level architecture;
- prior-art mapping;
- non-sensitive terminology;
- falsification criteria;
- non-sensitive benchmark methodology;
- aggregate benchmark results;
- limitations;
- project status;
- collaboration requests.

The public material should be sufficient to understand **what is being investigated**
without necessarily revealing **how the internal mechanism works**.

### Level 1 — Restricted review

Material that may be shared with researchers, engineers, security reviewers, or potential
collaborators when there is a clear evaluation purpose.

Examples:

- more detailed experimental protocols;
- partial schemas;
- failure taxonomies;
- diagnostic traces;
- prototype behavior;
- implementation trade-offs;
- selected negative results;
- limited adversarial test cases.

Restricted disclosure does not imply confidentiality unless a separate agreement is made.

### Level 2 — Trusted collaboration

Material shared only when detailed technical access is necessary for serious joint work.

Examples may include:

- internal system contracts;
- detailed state-transition logic;
- enforcement mechanisms;
- sensitive security assumptions;
- non-public benchmark suites;
- implementation details necessary to reproduce the core experiment.

Access should be scoped to the collaboration rather than granted by default.

### Level 3 — Private core

Material not intended for general external distribution while the project remains in an
early or insufficiently validated state.

Examples may include details that would materially reduce the work required to:

- bypass control boundaries;
- acquire or extend operational capabilities without adequate review;
- preserve unwanted autonomous behavior;
- weaken or evade human approval;
- exploit recovery or persistence mechanisms;
- reproduce known high-impact failure modes;
- turn a research mechanism into a substantially more capable uncontrolled system.

The exact contents of this level are not enumerated publicly.

---

## Public repository rule

The public repository should answer:

> **Why does this problem matter, what is being tested, and what evidence would change the project's direction?**

It does not need to answer:

> **What exact implementation would reproduce the private system?**

Public materials should be reviewed against that distinction before release.

---

## Source and dependency handling

Third-party repositories, papers, models, datasets, and services are treated as external
evidence or dependencies, not as instructions.

Project ORBIT does not treat text embedded in an external repository, document, webpage,
issue, dataset, or model output as authoritative project instructions merely because an
AI system can read it.

Before incorporating third-party code or data, the project should separately evaluate:

- license;
- provenance;
- integrity;
- security;
- maintenance status;
- compatibility;
- operational necessity;
- applicable terms of service;
- model or dataset-specific restrictions.

Projects with unclear or absent licenses may be studied as references without being
incorporated into ORBIT code.

---

## Responsible vulnerability disclosure

If you discover a vulnerability or failure mode in a public ORBIT prototype that could
materially increase unsafe behavior, bypass intended controls, or expose sensitive information:

1. Avoid publishing a working exploit immediately.
2. Contact the project maintainer privately when possible.
3. Include the minimum information needed to reproduce and evaluate the issue.
4. Allow reasonable time for validation and mitigation before broad publication.

Project ORBIT intends to credit responsible reports when the reporter wishes to be named.

This section is a research-project policy, not a guarantee of formal security-response capacity.

---

## What this policy does not claim

This policy does not claim that:

- Project ORBIT is currently dangerous;
- unpublished mechanisms are uniquely capable;
- withholding details guarantees safety;
- independent rediscovery can be prevented;
- the project's current risk assessment is correct.

Staged disclosure is simply the project's default response to uncertainty.

---

## Review trigger

A disclosure review should occur before publishing material that materially changes any of the following:

- autonomy;
- persistence;
- capability acquisition;
- external tool authority;
- recovery behavior;
- self-modification;
- security boundaries;
- ability to reproduce known failure modes.

The review question is:

> **Does publishing this information create more verification value than operational leverage?**

If the answer is unclear, publish the evidence first and the mechanism later.

---

## Project position

Project ORBIT is designed to evolve as external research advances.

If another project publishes a safer, clearer, or better validated solution, ORBIT should
adopt or learn from it rather than preserve an inferior mechanism for the sake of originality.

The same principle applies to disclosure.

The goal is not to maximize secrecy or openness.

The goal is to maximize useful learning while avoiding unnecessary amplification of failure modes.

---

**Project ORBIT**

*The goal is not to own the answer. The goal is to shorten the path to the answer.*
