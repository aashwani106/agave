# Permanent Course Rules

These rules apply to every new lesson. They are acceptance criteria, not suggestions.

## Public handbook and official-source rule

The course is written for the engineering community, not as personal notes. Use reader-neutral language and assume the handbook may be cloned independently from Agave.

All source references follow [SOURCE-POLICY.md](SOURCE-POLICY.md): link to the official [Anza Agave repository](https://github.com/anza-xyz/agave) at the full commit pinned in the root [Agave Version](README.md#agave-version), include symbol or line anchors when useful, and never publish branch-based or local-only source links. Every lesson includes **Official Code** and **Official Sources** sections.

## Curriculum prerequisite gate

Agave implementation lessons follow the Solana architecture prerequisite sequence. Before publishing a lesson, confirm that its underlying concept has already been introduced. Never pull a later concept forward merely because a source file references it.

Current curriculum alignment:

```text
Studying now
├── Banking Stage
├── Scheduler
├── Account Locks
└── Sealevel

Next externally
├── SVM
├── Broadcast
├── TVU
└── Consensus
```

This status is updated in [progress.md](progress.md) whenever curriculum prerequisites advance.

## Required lesson order

Every lesson follows this teaching sequence:

```text
Current Position
      ↓
Problem
      ↓
Why the component exists
      ↓
High-level architecture
      ↓
Execution flow
      ↓
Repository Explorer
      ↓
Code navigation and call graph
      ↓
Code walkthrough
      ↓
Rust encountered in that code
      ↓
Summary
      ↓
STOP HERE
```

Architecture must be understood before source syntax. Rust is introduced only when encountered.

## Required lesson contents

Every lesson must include:

- a **Current Position** tree with one exact `← YOU ARE HERE` marker;
- the problem and why Solana/Agave needs the component;
- high-level architecture and execution flow;
- a **Repository Explorer** listing relevant folders, relevant files, ignored areas, and why;
- caller, callees, execution path, responsibility, ownership, concurrency, failure, and performance boundaries;
- a code walkthrough that does not hide unexplained lines;
- just-in-time Rust explanations;
- ASCII architecture, Mermaid flow, sequence diagram, call graph, folder tree, and a memory diagram when useful;
- common mistakes and misconceptions;
- quiz, questions, exercises, and things to explore next;
- an explicit `STOP HERE` boundary.

If a diagram type would be misleading or genuinely adds no information, the lesson must say why rather than inserting decorative duplication.

## Repository navigation rule

No file is explained in isolation. For every studied file, state:

1. who calls into it;
2. what it calls;
3. where its input originated;
4. where its output goes;
5. who owns or borrows the important data;
6. its responsibility and what it deliberately does not own.

Ignored areas are listed to prevent accidental scope expansion, not to imply they are unimportant.

## Reverse-engineering mode

Every major subsystem includes a staged design explanation:

```text
minimal implementation
        ↓
improved implementation
        ↓
production implementation
        ↓
Agave implementation
```

Each step must identify the new failure, scale, correctness, or performance requirement that forced the added complexity. This belongs at the subsystem level; tiny boundary lessons need not invent a fake implementation progression.

## Reference collections

- `architecture/` contains only architectural claims established by completed lessons. Documents evolve incrementally.
- `code-index/` is a searchable encyclopedia of studied symbols and modules. Entries must include purpose, relevant files, entry points, call graph, dependencies, related modules, important structs, and important traits.
- Finishing a major subsystem creates that subsystem's `Contributing.md` with easy improvements, documentation opportunities, performance ideas, good-first-issue candidates, tests, debugging tips, and repository conventions.

Potential bugs and performance ideas must be labeled as hypotheses until verified with evidence.

## Stop rule

Never create the next lesson automatically. At the end of a lesson:

1. present the quiz, questions, exercises, and common mistakes;
2. mark `STOP HERE`;
3. update progress;
4. wait for an explicit request to continue.
