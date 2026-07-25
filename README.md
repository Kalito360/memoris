# Memoris

**Verifiable memory infrastructure for AI agents — built on [Shelby](https://shelby.xyz).**

## The problem

AI agents make decisions constantly — trading bots, autonomous assistants, robotics agents — but nobody can independently verify what an agent actually knew at the time it made a decision. Today's agent memory lives in centralized databases that can be edited, deleted, or rewritten after the fact. When something goes wrong, there's no way to prove what was true.

## What Memoris does

Memoris gives AI agents a way to store memory with a **cryptographic receipt** attached to every write — provable, tamper-evident, and independently verifiable after the fact.

Memoris does not reinvent storage, hashing, or blockchain anchoring. It sits **on top of Shelby's verifiable global object storage**, adding the structure and developer experience that's specific to agent memory:

- Agent- and session-aware memory objects (not just generic files)
- A simple SDK: `store()`, `retrieve()`, `verify()`
- A dashboard for exploring an agent's memory history and verification status
- A verification flow that lets anyone confirm: *"this agent's memory contained exactly this information at this time, unmodified since"*

Shelby provides the storage, the cryptographic proof, and the Aptos anchoring. Memoris provides the agent-memory abstraction and verification UX on top of it.

## Why build this on Shelby

Shelby is purpose-built for exactly the kind of read-heavy, globally-distributed, verification-critical workload that agent memory requires — single global namespace, cryptographic proof on every read, S3-compatible SDKs. Rather than build a parallel storage and verification stack, Memoris treats Shelby as its foundation and focuses entirely on the agent-specific layer that doesn't exist yet.

## Status

Early-stage. Architecture and design in progress. Looking to integrate against Shelby's Early Access API/SDK as it becomes available.

## Roadmap (high level)

- [ ] Phase 1 — Architecture, schema, API spec
- [ ] Phase 2 — Backend orchestration + Shelby integration layer
- [ ] Phase 3 — Verification engine (pass-through to Shelby's proof system)
- [ ] Phase 4 — Dashboard (agent explorer, verification portal)
- [ ] Phase 5 — Python + TypeScript SDKs
- [ ] Phase 6 — Deployment
- [ ] Phase 7 — Documentation

## Get involved

This project is being built in the open. Feedback, questions, and collaboration are welcome.
