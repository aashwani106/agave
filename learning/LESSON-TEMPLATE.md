# Lesson NN — Component Name

> **Status:** Draft | Published | Needs source refresh  
> **Agave baseline:** [repository baseline](README.md#agave-version), or documented module override `<40-character SHA>`  
> **Version note:** identify implementation details likely to change in later Agave versions.

## Current Position

Add an architecture tree with exactly one `← YOU ARE HERE` marker. State established prerequisites and excluded later concepts.

## Problem

What concrete correctness, scale, latency, availability, or operability problem is being solved?

## Why This Component Exists

Why does Solana need it? What becomes insufficient without it? Use an analogy only when it clarifies the mechanism.

## High-Level Architecture

Include scoped ASCII and Mermaid diagrams. Define responsibility and non-responsibilities.

## Execution Flow

Show input origin, transformations, output destination, failure paths, and a sequence diagram.

## Repository Explorer

List linked relevant official directories/files and explain why each exists. List intentionally ignored areas and why entering them would break scope.

## Official Code

- [Relevant directory](https://github.com/anza-xyz/agave/tree/COMMIT_HASH/path)
- [Relevant file](https://github.com/anza-xyz/agave/blob/COMMIT_HASH/path/file.rs)
- [`ImportantStruct`](https://github.com/anza-xyz/agave/blob/COMMIT_HASH/path/file.rs#Lx-Ly)
- [`important_function()`](https://github.com/anza-xyz/agave/blob/COMMIT_HASH/path/file.rs#Lx-Ly)

## Code Navigation

Explain callers, callees, call graph, responsibility, input/output ownership, borrowing, concurrency, thread safety, performance choices, and failure behavior. No file is isolated.

## Reverse Engineering the Design

For a major subsystem, explain `minimal → improved → production → Agave` and the requirement forcing each increase in complexity. For a small boundary lesson, explain why this is deferred to its parent subsystem.

## Code Walkthrough

Walk official source in bounded ranges. Link every explained function, struct, enum, trait, and range. Explain every relevant line and mark intentionally skipped generated, test-only, or unrelated code.

## Rust Encountered

Explain only syntax and semantics required by the walkthrough, including ownership and borrowing effects.

## Memory and Data Model

Add an ownership/memory diagram when useful. If not useful, state why.

## Important Structs, Enums, and Traits

For each symbol: official source link, purpose, fields/variants or required methods, owner, lifecycle, and thread-safety implications.

## Common Mistakes and Misconceptions

List likely incorrect mental models and corrections.

## Summary

Restate the problem, boundary, execution path, and debugging entry point without new material.

## Official Sources

- **Agave source:** links used above.
- **Pull requests/issues:** relevant design history, or “None required for this lesson.”
- **Anza/Solana documentation:** relevant official documentation, or “None required.”
- **SIMDs/RFCs:** applicable links, or “Not applicable.”
- **Research:** original paper links, or “Not applicable.”

## Quiz

Include conceptual, architecture, code-navigation, and ownership questions.

## Questions for Further Study

Record questions deliberately outside scope.

## Exercises

Include source navigation, call tracing, ownership tracing, test discovery, and one small design exercise.

## STOP HERE

State the completion test. Do not begin or generate the next lesson.
