# Project ORBIT — Status

**Public status:** Early research / prototype design  
**Last updated:** 2026-09-05  
**Repository type:** Public research surface  
**Disclosure level:** Level 0 — Public

---

## Current position

Project ORBIT is currently investigating whether a persistent systems layer can preserve important properties across:

- model replacement,
- runtime replacement,
- tool changes,
- process interruption,
- long-horizon execution,
- and capability growth.

The project is **not** currently claiming a finished architecture, a production system, or an AGI system.

The public repository intentionally omits implementation details that would allow the private mechanism to be reconstructed.

---

## Current working thesis

> **Some system-level properties should remain stable even when the underlying model, runtime, tools, and implementation mechanisms change.**

The project is currently testing whether this thesis can be made operational, measurable, and backend-independent.

---

## Current research stage

### Stage 0 — Problem framing
**Status:** COMPLETE

Questions established:

- What must persist beyond a single model session?
- What should remain stable when the model changes?
- Which parts belong to the model, and which parts belong to the surrounding system?
- Which existing agent/runtime capabilities should be reused rather than rebuilt?

### Stage 1 — Prior-art convergence mapping
**Status:** ACTIVE / SUBSTANTIALLY COMPLETE

The project has identified strong adjacent work in:

- Agent OS architectures;
- durable agent execution;
- persistent state and memory;
- agent lifecycle management;
- governance and control layers;
- self-improving agent scaffolds;
- tool/capability interfaces.

The current conclusion is that ORBIT should **not** attempt to reproduce the entire surrounding stack.

Where high-quality external infrastructure exists, reuse is preferred.

### Stage 2 — Minimal falsifiable hypothesis
**Status:** ACTIVE

The current objective is to reduce ORBIT to the smallest system-level hypothesis that can be experimentally falsified.

Public criteria include:

- measurable reduction of a defined failure class;
- survival of the same property across backend replacement;
- survival of the same property across model replacement;
- consistent reconstruction of consequential behavior;
- persistent measurable gain after capability acquisition.

The private mechanism being tested against these criteria is not disclosed here.

### Stage 3 — Minimal executable prototype
**Status:** NOT YET PUBLICLY VALIDATED

The intended first prototype is deliberately small.

It should demonstrate:

1. a persistent system state;
2. at least one replaceable model/runtime boundary;
3. one consequential tool action;
4. one enforceable system-level constraint;
5. one failure scenario;
6. one reproducible result.

A larger feature set is not currently considered a success criterion.

### Stage 4 — Adversarial evaluation
**Status:** PLANNED

The project intends to test whether the proposed layer survives:

- conflicting information;
- stale or invalid state;
- model disagreement;
- process interruption;
- backend substitution;
- capability changes;
- deliberate attempts to violate assumptions.

Only non-sensitive benchmark descriptions and aggregate results will be published by default.

### Stage 5 — Capability growth
**Status:** RESEARCH DIRECTION / NOT VALIDATED

A longer-term direction is controlled capability acquisition.

At public resolution, the idea is:

> A persistent system detects a capability gap, evaluates available options, and attempts to acquire or construct the missing capability in a way that produces measurable persistent improvement.

This is **not** a claim of safe self-improvement or unrestricted autonomy.

The operational mechanism is not public.

---

## What is frozen

The following are current public project commitments:

### F-01 — Replaceability
No specific foundation model should define the identity of the system.

### F-02 — Reuse over reinvention
Existing infrastructure should be reused when it satisfies the required system contract.

### F-03 — Measurability
A proposed ORBIT property must eventually be testable.

### F-04 — Falsifiability
If the property produces no measurable improvement, the hypothesis should be revised or discarded.

### F-05 — Controlled consequences
Increasing capability must not automatically imply increasing authority.

### F-06 — Staged disclosure
Evidence and evaluation may be public before sensitive operational mechanisms are public.

### F-07 — Mechanism replaceability
Implementation mechanisms may change without requiring the project thesis to change.

These commitments may still be revised if evidence shows they are wrong, but they should not drift silently.

---

## What is explicitly not frozen

The following remain open:

- exact runtime backend;
- model provider;
- storage backend;
- workflow engine;
- memory implementation;
- agent framework;
- scheduler;
- deployment model;
- internal representation;
- benchmark suite;
- self-extension mechanism;
- terminology.

The project expects many of these to change.

---

## Current reuse strategy

| Area | Current strategy |
|---|---|
| Foundation models | External / replaceable |
| Durable execution | Prefer existing runtime |
| Checkpointing | Prefer existing runtime |
| Tool protocol | Prefer existing standards |
| Persistent storage | External backend |
| Multi-agent infrastructure | External or optional |
| Observability | External infrastructure |
| ORBIT-specific system properties | Direct research |
| Sensitive control logic | Private until justified for broader disclosure |

---

## Current public baselines / adjacent systems

The project is tracking work including:

- AIOS
- AOS
- LangGraph
- Microsoft AutoGen
- Temporal
- Letta
- Model Context Protocol
- self-improving-agent research
- other durable agent-runtime projects

These systems are not treated as competitors by default.

They are potential:

- substrates,
- baselines,
- prior art,
- reusable components,
- and sources of falsifying evidence.

---

## Resource status

Project ORBIT is currently **resource-constrained**.

The highest-value forms of support are:

- compute / API credits;
- access to realistic benchmark environments;
- technical review;
- security and reliability review;
- engineering help on non-core infrastructure;
- temporary experiment infrastructure.

The project does not currently require a large organizational commitment to make progress.

A bounded experiment is preferable to a vague partnership.

---

## Current collaboration target

A useful first collaboration would be one of the following:

1. review the restricted technical brief;
2. select one existing agent runtime;
3. define one adversarial benchmark;
4. run a bounded comparison;
5. stop if the result is null;
6. expand only if the signal survives.

---

## Public milestone definition

The next meaningful public milestone is **not**:

- more diagrams,
- more terminology,
- more agents,
- more integrations,
- or a larger repository.

It is:

> **A reproducible experiment showing whether one ORBIT system-level property survives contact with an existing agent runtime.**

---

## Status summary

| Item | State |
|---|---|
| Problem framing | Complete |
| Prior-art mapping | Active / strong coverage |
| Public project thesis | Defined |
| Disclosure policy | Defined |
| Reuse policy | Defined |
| Minimal falsifiable hypothesis | Active |
| Minimal prototype | In progress / not publicly validated |
| Adversarial benchmark | Planned |
| Cross-backend evaluation | Planned |
| Controlled capability growth | Research direction |
| AGI claim | None |

---

## Project rule

> **Do not preserve an ORBIT mechanism merely because ORBIT created it.**

If external research produces a better solution, use it.

If an experiment invalidates an internal assumption, remove it.

If several independent projects converge on the same result, treat convergence as information.

---

**Project ORBIT**

**What survives when the model changes?**

*The goal is not to own the answer. The goal is to shorten the path to the answer.*
