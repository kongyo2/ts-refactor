---
name: ts-refactor-jev
description: Refactor a TypeScript codebase, starting from a similarity-ts-jev duplication report.
---

# TypeScript refactor

## First action

From the repository root, before any other tool call, run exactly:

```bash
npx @kongyo2/similarity-ts-jev --min-score 0 .
```

Run it as written, with no grep, script, or other tool in its place, and read the entire output before doing anything else. The one addition it takes is `--output <path>`, for when the tool result is truncated; then read that file to the end.

This step is rigid because the report replaces your own guess about where the duplication is: it matches declarations after renaming and style canonicalization, so the pairs it lists are invisible to grep and to reading the likely files.

## The report

The report is evidence, not a target. 