# Project ORBIT — Research Context

**Last updated:** 2026-09-05  
**Scope:** Public research context only  
**Purpose:** Position ORBIT relative to adjacent work without exposing the private mechanism

---

## Overview

Project ORBIT is not being developed in isolation.

Several research and engineering communities are independently moving toward systems that combine:

- long-running agents,
- persistent state,
- tool use,
- model routing,
- durable execution,
- governance,
- capability control,
- and self-improvement.

ORBIT treats this convergence as evidence that a new systems boundary may be emerging above individual foundation models.

The project does **not** claim ownership of that boundary.

Its research interest is narrower:

> **Which properties must remain stable across replaceable models, runtimes, tools, and implementation mechanisms?**

---

# 1. Agent Operating Systems

## AIOS: LLM Agent Operating System

**Paper:** *AIOS: LLM Agent Operating System*  
**arXiv:** 2403.16971  
**Published:** 2024

AIOS proposes moving resource management and LLM-specific services out of individual agents and into an AIOS kernel.

Publicly described kernel responsibilities include:

- scheduling;
- context management;
- memory management;
- storage management;
- access control;
- LLM resource management;
- external tool management.

### Relevance to ORBIT

AIOS is strong evidence that:

> **The model/agent application does not need to own all of its execution infrastructure.**

This overlaps significantly with any broad claim that ORBIT is simply an "AI operating system."

Therefore:

- ORBIT does not treat the Agent OS concept itself as novel;
- AIOS is considered prior art and a possible experimental reference;
- ORBIT should avoid rebuilding generic resource-management functions without a specific reason.

### Public reference

https://arxiv.org/abs/2403.16971

---

## The Agent Operating System (AOS)

**Paper:** *The Agent Operating System (AOS): A Reference Operating Architecture for Distributed Agentic Systems*  
**arXiv:** 2608.03214  
**Published:** 2026

AOS proposes a vendor-neutral reference architecture with two major internal planes.

### Control & Governance Plane

Publicly described concerns include:

- intent;
- policy;
- trust;
- authority;
- confidence;
- auditability;
- observability;
- human oversight.

### Runtime & Coordination Plane

Publicly described concerns include:

- agent lifecycle;
- workflow coordination;
- model routing;
- tool routing;
- context;
- memory;
- scheduling;
- traffic management;
- runtime assurance.

The paper explicitly keeps operating systems such as Linux/Windows and container/runtime infrastructure outside the AOS boundary.

### Relevance to ORBIT

AOS is particularly important because it moves beyond generic agent orchestration and treats:

- governance,
- authority,
- uncertainty,
- audit,
- and runtime coordination

as part of one operating architecture.

This means ORBIT cannot rely on the existence of a governance layer alone as its distinguishing research claim.

Instead, AOS is a strong baseline for asking:

> What system property, if any, remains insufficiently specified or enforced after adopting such a reference architecture?

### Public reference

https://arxiv.org/abs/2608.03214

---

# 2. Durable Agent Execution

## LangGraph

LangGraph provides a persistence layer based on checkpoints and thread state.

Public documentation describes support for:

- persistence;
- human-in-the-loop workflows;
- memory across interactions;
- time-travel debugging;
- fault tolerance;
- recovery from interrupted execution.

### Relevance to ORBIT

This substantially reduces the need for ORBIT to invent:

- generic checkpoint systems;
- generic resume logic;
- generic graph persistence;
- basic human-interrupt infrastructure.

ORBIT should instead test whether its own system-level properties can survive when LangGraph is used as an execution substrate.

### Public reference

https://docs.langchain.com/oss/python/langgraph/persistence

---

## Temporal

Temporal is a mature durable-execution platform.

It is not specific to AI agents, which makes it especially useful as a reminder that:

> Durable execution is not an AI-specific invention.

### Relevance to ORBIT

If ORBIT requires persistent workflows, retries, crash recovery, or long-running execution, those capabilities should be treated as infrastructure unless the project has a specific system property that cannot be expressed using existing durable-execution substrates.

Temporal is therefore a possible backend, not a research target by default.

---

# 3. Agent Runtime and Lifecycle

## Microsoft AutoGen

AutoGen provides a runtime model for agents and supports local and distributed execution.

Its public architecture discusses:

- agent identity;
- lifecycle;
- message delivery;
- runtime environments;
- security and privacy boundaries;
- distributed execution.

### Relevance to ORBIT

AutoGen demonstrates that:

> Agent identity and lifecycle can already be owned by a runtime rather than by an individual model call.

Therefore ORBIT should not treat generic lifecycle ownership or multi-agent communication as a sufficient research contribution.

A useful ORBIT experiment would test whether a higher-level system property remains invariant when AutoGen is substituted for another runtime.

### Public reference

https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/core-concepts/architecture.html

---

# 4. Persistent Memory and Stateful Agents

## Letta and related memory systems

Persistent-agent systems increasingly separate model execution from long-term agent state.

Common capabilities include:

- long-term memory;
- persistent agent identity/state;
- state editing;
- tool use;
- context management.

### Relevance to ORBIT

ORBIT should not treat the existence of persistent memory as novel.

The open research question is not:

> Can an agent remember?

It is closer to:

> What does persisted information mean to the surrounding system, and under what conditions should that information affect consequential behavior?

The exact ORBIT interpretation of this question is not part of the public disclosure.

---

# 5. Tool and Capability Interfaces

## Model Context Protocol (MCP)

MCP provides a standardized interface between AI applications and external resources/tools.

### Relevance to ORBIT

MCP reduces the value of inventing another generic tool protocol.

ORBIT can treat MCP and similar protocols as external interfaces.

The research interest lies above the protocol:

- when a capability should be available;
- how the system reasons about capability changes;
- how consequential use should be evaluated.

The public repository does not disclose the internal mechanism used for these decisions.

---

# 6. Self-Improving Agent Systems

## Self-Improvements in Modern Agentic Systems

**Paper:** *Self-Improvements in Modern Agentic Systems: A Survey*  
**arXiv:** 2607.13104  
**Published:** 2026

This survey frames a modern agent as a system composed of:

- a foundation model;
- prompts;
- memory;
- tools;
- control logic.

It treats improvement as persistent updates not only to model parameters but also to the surrounding operational scaffold.

Examples of scaffold-level change include:

- memory changes;
- prompt changes;
- tool changes;
- executable logic changes;
- control changes.

### Relevance to ORBIT

This is important because ORBIT's longer-term capability-growth direction should not be presented as if system-level self-improvement were an unexplored idea.

The useful research question becomes narrower:

> Can capability growth be controlled, persisted, evaluated, and retained without collapsing capability into unrestricted authority?

The concrete mechanism remains private.

### Public reference

https://arxiv.org/abs/2607.13104

---

# 7. AGI Context

## Capability-oriented definitions

The DeepMind *Levels of AGI* framework emphasizes observable capability rather than a particular architecture.

Relevant dimensions include:

- generality;
- performance;
- autonomy.

### Relevance to ORBIT

ORBIT does not currently make an AGI claim.

A persistent, self-extending architecture is not sufficient evidence of general intelligence.

If ORBIT ever becomes relevant to AGI evaluation, that relevance must come from demonstrated cross-domain capability, transfer, performance, and autonomy—not from terminology such as:

- Cognitive OS;
- Agent OS;
- self-improvement;
- self-extension.

### Public reference

https://research.google/pubs/levels-of-agi-operationalizing-progress-on-the-path-to-agi/

---

# 8. Convergence map

At public resolution, the surrounding landscape looks approximately like this:

```text
                   Agentic Systems

        ┌─────────────────────────────┐
        │     Governance / Control    │
        │          AOS, etc.          │
        └──────────────┬──────────────┘
                       │
     ┌─────────────────┼──────────────────┐
     │                 │                  │
Agent OS          Durable Runtime    Stateful Agents
 AIOS            LangGraph/Temporal      Letta
     │                 │                  │
     └─────────────────┼──────────────────┘
                       │
                Tool Interfaces
                     MCP
                       │
                 Models / Tools
```

ORBIT is intentionally **not** attempting to own every box in this diagram.

Its research thesis concerns a property that should remain stable **across** these boxes.

The private mechanism is not represented in this public map.

---

# 9. What ORBIT will reuse

The project currently prefers reuse for:

- model inference;
- generic scheduling;
- durable workflow execution;
- checkpointing;
- storage;
- tool protocols;
- multi-agent communication;
- sandboxing;
- observability;
- standard databases.

Where appropriate, ORBIT may use adapters rather than copies or forks.

---

# 10. What ORBIT must still demonstrate

The existence of adjacent research does not validate ORBIT.

The project must still demonstrate that:

1. there is a measurable system-level failure class worth addressing;
2. the proposed ORBIT layer materially changes that failure rate;
3. the property survives backend replacement;
4. the property survives model replacement;
5. the mechanism does not create unacceptable false blocking or operational cost;
6. persistent capability growth, if pursued, produces real improvement rather than configuration churn.

Until then, ORBIT remains an experimental architecture hypothesis.

---

# 11. Why convergence is useful

ORBIT does not treat convergence as evidence that the project should stop.

If independent groups repeatedly discover the same components, several possibilities exist:

### Case A — The external solution is better
Adopt it.

### Case B — The result fully eliminates an ORBIT research question
Remove that question.

### Case C — Most of the problem is solved, but a residual failure remains
Study the residual.

### Case D — ORBIT's hypothesis produces no measurable difference
Discard or revise it.

This is the intended development loop.

---

# 12. Research posture

Project ORBIT follows a simple rule:

> **Do not defend an internal mechanism merely because it originated inside ORBIT.**

Prior art is not an obstacle.

It is compressed research time.

External implementation is not a threat.

It is saved engineering effort.

Convergence is not a loss of originality.

It is evidence about the shape of the problem.

---

# 13. Public references

1. **AIOS: LLM Agent Operating System**  
   https://arxiv.org/abs/2403.16971

2. **The Agent Operating System (AOS): A Reference Operating Architecture for Distributed Agentic Systems**  
   https://arxiv.org/abs/2608.03214

3. **LangGraph Persistence**  
   https://docs.langchain.com/oss/python/langgraph/persistence

4. **Microsoft AutoGen — Agent Runtime Architecture**  
   https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/core-concepts/architecture.html

5. **Self-Improvements in Modern Agentic Systems: A Survey**  
   https://arxiv.org/abs/2607.13104

6. **Google DeepMind — Levels of AGI**  
   https://research.google/pubs/levels-of-agi-operationalizing-progress-on-the-path-to-agi/

---

## Scope note

This document describes **publicly visible research context**.

It does not identify:

- the private ORBIT state model;
- the specific internal system property currently under test;
- internal transition semantics;
- sensitive benchmark cases;
- enforcement mechanisms;
- capability-acquisition logic.

Those details are governed by the repository's disclosure policy.

---

**Project ORBIT**

**What survives when the model changes?**

*The goal is not to own the answer. The goal is to shorten the path to the answer.*
