# Contributing to the Agave Internals Handbook

Contributions should make Agave easier to understand without sacrificing technical accuracy.

## Useful contributions

- correct a source or architecture explanation;
- migrate a module deliberately to a newer verified upstream commit;
- add a commit-pinned version note;
- improve a diagram or ownership explanation;
- add a focused exercise, test-navigation task, or debugging scenario;
- document an upstream architectural change;
- improve accessibility, terminology, or prerequisite guidance.

## Requirements

1. Follow [COURSE-RULES.md](COURSE-RULES.md) and [SOURCE-POLICY.md](SOURCE-POLICY.md).
2. Link every code-specific explanation to the official [Anza Agave repository](https://github.com/anza-xyz/agave) using the full commit in the root [Agave Version](README.md#agave-version), unless a module override is documented.
3. Preserve architecture-before-code ordering and lesson scope.
4. Separate stable concepts from evolving implementation details.
5. Explain new Rust syntax only where encountered.
6. Do not present unverified performance or bug claims as facts.
7. Do not publish local paths, credentials, validator identities, ledger contents, or private operational data.

## Proposing a lesson change

Include the gap being fixed, official source evidence, Agave commit/date used for verification, affected diagrams/indexes, and behavior that differs across versions or platforms.

## Reporting a mistake

Report the lesson and section, incorrect statement, official source link demonstrating the issue, observed Agave commit/date, and a suggested correction if known.

## Repository conventions

- Use lowercase kebab-case lesson directories and descriptive Markdown filenames.
- Use relative links for handbook pages and commit-pinned official HTTPS permalinks for Agave source.
- Keep diagrams readable without requiring a particular editor.
- Give symbols code formatting and links on their first substantive explanation.
- Update code-index and architecture notes only with material established by a lesson.
- Create a subsystem `Contributing.md` only when that subsystem has been completed.
