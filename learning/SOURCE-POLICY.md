# Official Source and Versioning Policy

## Canonical repository

All Agave source citations point to the official repository: <https://github.com/anza-xyz/agave>.

Do not publish local filesystem links, editor links, mirrors, copied source files, or links that require access to an author's checkout.

## Pinned baseline

The current commit, workspace version, date, and release status are declared once in the root [README](README.md#agave-version). That section is the source of truth for the handbook baseline.

Do not link source explanations to a branch name such as `master`, `main`, or a release branch. Branches move and can silently invalidate line-level explanations.

## Link format

Use official GitHub links whenever a source file, directory, module, function, struct, enum, trait, constant, or relevant code range is discussed.

- File: `https://github.com/anza-xyz/agave/blob/<commit>/<path>`
- Lines: `https://github.com/anza-xyz/agave/blob/<commit>/<path>#Lx-Ly`
- Directory: `https://github.com/anza-xyz/agave/tree/<commit>/<path>`
- Pull request: `https://github.com/anza-xyz/agave/pull/<number>`

Prefer descriptive Markdown labels, for example:

```markdown
[`main()` in `validator/src/main.rs`](https://github.com/anza-xyz/agave/blob/3b1b239ce2ae3868dce17ff0e06fd0ac32313592/validator/src/main.rs#L17-L138)
```

Repository trees and diagrams may show short paths for spatial orientation. The same paths must be linked immediately below the diagram or in the adjacent **Official Code** list.

## Permalinks and reproducibility

Every code walkthrough must identify the root baseline or declare an explicit module-specific override. Exact line commentary always uses a full 40-character commit hash. Short hashes and tags are useful labels but are not source permalinks.

The unpinned repository homepage may be linked for general navigation. Code, trees, symbols, and line ranges must be pinned.

Conceptual explanations must not imply that the pinned implementation is protocol-mandated or eternally current. Label implementation details, feature-gated behavior, platform differences, and known historical changes explicitly.

## Updating Agave

Update modules deliberately:

1. choose and verify a new official commit;
2. compare affected source and behavior;
3. update explanations, diagrams, exercises, and index entries;
4. replace permalinks only after review;
5. update the root version table, or document a temporary module override;
6. record meaningful implementation changes in the affected lesson.

## Required lesson references

Every lesson contains both sections:

### Official Code

Links to relevant official Agave files, directories, modules, and precise symbols/ranges used by the walkthrough.

### Official Sources

As applicable, links to official Agave source, pull requests and issues, Anza and Solana documentation, SIMDs or RFCs, specifications, and research papers. If a category is not applicable, say so. Do not add decorative or weakly related references merely to fill the list.

## Source quality

Prefer official Agave source, then accepted specifications and official documentation, then official design history, and finally original research. Clearly label secondary explanations and inferences. Potential bugs and performance ideas remain hypotheses until reproduced or supported by measurements.
