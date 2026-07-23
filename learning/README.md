# The Agave Internals Handbook

An open-source, source-guided course for engineers who want to understand, navigate, debug, and contribute to the [Agave validator](https://github.com/anza-xyz/agave).

Agave is Anza's validator client implementation for the Solana protocol. It contains the production systems that ingest transactions, schedule and execute work, maintain accounts, produce and replay blocks, communicate across the cluster, vote, and expose operator services. This handbook teaches those systems incrementally instead of presenting the repository as one enormous directory tour.

## Agave Version

This is the handbook's single source of truth for its current source baseline.

| Field | Baseline |
|---|---|
| Repository | [anza-xyz/agave](https://github.com/anza-xyz/agave) |
| Commit | [`3b1b239ce2ae3868dce17ff0e06fd0ac32313592`](https://github.com/anza-xyz/agave/commit/3b1b239ce2ae3868dce17ff0e06fd0ac32313592) |
| Workspace version | `4.3.0-alpha.1` |
| Commit date | 2026-07-14 |
| Release status | Development/alpha baseline; not represented as a tagged stable release |

All source links use this commit. Modules can move to a newer baseline incrementally, but any temporary mixed-version state must be recorded here and in the affected module.

## Who this handbook is for

The primary audience is an engineer who understands backend development and basic blockchain concepts but may be new to Rust, validator clients, or Solana core development. Rust is explained just in time, when a language feature appears in the source being studied.

The end goal is practical competence:

> Confidently navigate, understand, debug, and contribute to Agave.

## Recommended prerequisites

- experience building or operating backend services;
- basic knowledge of transactions, blocks, peer-to-peer networks, and consensus;
- willingness to read production Rust alongside each lesson;
- a local clone of the [official Agave repository](https://github.com/anza-xyz/agave) for search and experimentation.

Deep Rust experience is not required. Solana architecture concepts should be learned before their Agave implementations; the curriculum records these prerequisites in the [roadmap](00-roadmap/README.md).

## How the course is structured

Each lesson begins with its exact position in the validator architecture, explains the problem and architecture before code, narrows the relevant repository surface, and then walks through official Agave source. Lessons include execution flows, call graphs, ownership and memory models, failure boundaries, exercises, and a hard stop before the next topic.

- [Course roadmap](00-roadmap/README.md) — dependency order and current boundary.
- [Course rules](COURSE-RULES.md) — permanent teaching and scope requirements.
- [Lesson template](LESSON-TEMPLATE.md) — required structure for new lessons.
- [Architecture notes](architecture/README.md) — an evolving model containing only established material.
- [Code index](code-index/README.md) — searchable entries for studied symbols and modules.
- [Source policy](SOURCE-POLICY.md) — how official code and external references are cited.
- [Contributing](CONTRIBUTING.md) — how to improve explanations or report mistakes.

## How to follow along

1. Open the lesson currently identified in the [roadmap](00-roadmap/README.md).
2. Open its **Official Code** links in the [official Agave repository](https://github.com/anza-xyz/agave).
3. If doing local experiments, clone Agave separately and check out the pinned commit in **Agave Version** above.
4. Read architecture and execution flow before opening the walkthrough.
5. Complete the quiz and navigation exercises at `STOP HERE`.
6. Continue only after the underlying Solana concept is understood.

## Verifying explanations

Agave evolves. Every code-specific claim should be checked against its official permalink. Lessons distinguish stable concepts from implementation details and call out known version changes. Updating the handbook baseline is an explicit, module-by-module maintenance operation rather than an automatic movement with `master`.

The citation and versioning rules are defined in [SOURCE-POLICY.md](SOURCE-POLICY.md).

## Contributing and reporting mistakes

Corrections, clearer diagrams, stronger source citations, exercises, and version-update notes are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for repository conventions and the mistake-report template. Explanations should be supported by official code, official documentation, accepted SIMDs/RFCs where applicable, or clearly identified research sources.

## Current published lesson

[Lesson 01 — The validator as a process](01-introduction/README.md)

The course is stopped at the end of Lesson 01. No subsequent lesson is published yet.
