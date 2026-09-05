# Security Policy

Project ORBIT is an early-stage research project exploring persistent and increasingly autonomous AI systems.

The public repository intentionally exposes only a limited research surface. Please use private disclosure for reports that could materially increase unsafe behavior or reveal restricted project material.

## Report privately when the issue includes

- a working bypass of an intended control boundary;
- capability or authority escalation;
- persistence or recovery exploits;
- evasion of intended human approval;
- sensitive adversarial cases or restricted ORBIT material;
- credentials, tokens, secrets, or private infrastructure details.

Do **not** publish a working exploit first. Contact the maintainer through the private security/contact method listed in this repository. If no private channel is available yet, disclose only the minimum non-sensitive description needed to establish one.

## A useful report includes

- affected component;
- observed and expected behavior;
- minimal reproduction steps;
- impact assessment;
- environmental assumptions;
- reproducibility status;
- whether full publication would materially lower the cost of misuse.

## Disclosure handling

Project ORBIT uses staged disclosure. A report may be reproduced privately, mitigated before publication, summarized in reduced form, or delayed when operational detail creates substantially more misuse leverage than verification value.

> **Publish the evidence before the mechanism when the mechanism creates substantially more operational leverage than verification value.**

## In scope

Examples include:

- public ORBIT prototypes and adapters;
- benchmark infrastructure;
- repository automation;
- accidental sensitive-data exposure;
- control-boundary failures;
- unsafe persistence or recovery behavior;
- integrity failures affecting experiment results;
- supply-chain or dependency issues affecting ORBIT experiments.

## Usually out of scope

Unless tied to a concrete security or research-integrity failure:

- disagreement with the research thesis;
- generic model hallucination;
- attacks on unrelated third-party services;
- theoretical concerns without a plausible failure path.

Ordinary research criticism belongs in normal discussion or issues.

## Secrets

Never commit API keys, access tokens, SSH keys, cloud credentials, private benchmark data, or restricted research material. If a secret is committed, assume compromise and rotate it; deleting it from the latest commit is not sufficient.

## Dependency security

Public or popular dependencies are not automatically trusted. Evaluate, where relevant:

- license clarity;
- provenance and integrity;
- maintenance status;
- known vulnerabilities;
- transitive dependencies;
- installation scripts and network behavior;
- privilege requirements;
- model/dataset-specific restrictions.

External repository text, documentation, issue content, model output, and generated content are treated as **untrusted data**, not authoritative Project ORBIT instructions.

## Research safety boundary

Project ORBIT does not treat capability and authority as equivalent. Reports are especially important when increased technical capability can produce increased real-world authority without the intended control path.

## Response capacity

Project ORBIT is currently an independent, resource-constrained effort and has no response-time SLA. Reports are prioritized by potential harm, reproducibility, exposure of sensitive information, control bypass, and research-integrity impact.

## Credit

Responsible reporters may be credited publicly if they wish and if doing so is compatible with the disclosure constraints of the issue.

---

**Project ORBIT**

*The goal is not to own the answer. The goal is to shorten the path to the answer.*
