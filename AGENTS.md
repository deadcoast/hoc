# Repository Guidelines

## Project Structure & Module Organization

The canonical CAH 0.0.4 specification lives in `0.0.4/`, where the two-digit numeric prefix encodes the document sequence: `0.0.4-01-OVERVIEW.md` introduces the model, `0.0.4-02-GRAMMAR.md` to `0.0.4-07-ALGORITHM.md` define mechanics, while `0.0.4-08-TEST-MANIFEST.md` onward capture validation artifacts. Keep related additions grouped by index so cross-references (e.g., the ASCII spine diagram) stay stable. Use `0.0.4/Tasks-TODO/` to track in-flight edits, edge cases, and revision notes before promoting them into the normative files.

## Build, Test, and Development Commands

This repository is documentation-first; no compiled artifacts are generated. Before opening a PR, run local hygiene checks such as `markdownlint "0.0.4/**/*.md"` and `rg --files-with-matches "TODO" 0.0.4` to surface unfinished work. When diagrams change, rebuild context tables by re-running any helper scripts referenced in the Tasks list or restating the derivation explicitly inside the affected file.

## Coding Style & Naming Conventions

Author content in Markdown with plain ASCII diagrams; keep indentation consistent with existing examples (two-space indentation inside lists, fenced code blocks for grammar or schemas). Reuse canonical abbreviations from `0.0.4-01-OVERVIEW.md` (`CHO`, `ACT`, `ABT`, etc.) and mirror the all-caps filename pattern `0.0.4-XX-TITLE.md` for new modules. Introduce new terms via a local dictionary block before applying them elsewhere, and cross-link using bolded labels rather than raw URLs unless pointing outside the spec.

## Testing Guidelines

Every normative change that affects evaluation must update `0.0.4-08-TEST-MANIFEST.md` with new scenario IDs, align the schema in `0.0.4-09-TEST-OUTCOME-SCHEMA.md`, and document any validator adjustments in `0.0.4-15-INCREMENTAL-VALIDATION.md` or `0.0.4-16-PROPERTY-BASED-TEST.md`. Snapshot expected outputs by appending tables or code blocks that mirror the reference bundle format so reviewers can diff behavior without executing tooling.

## Commit & Pull Request Guidelines

Commits follow the descriptive, present-tense style already in history (e.g., “Update normative artifacts…”). Summaries should state the scope (document IDs or glossary section) and the intent (clarify, add scenario, revise schema). In PR descriptions, list touched files, note impacts to downstream validators, and reference any Tasks entries closed. Attach rendered Markdown screenshots only when diagrams or complex tables change; otherwise link to the file section (e.g., `0.0.4-07-ALGORITHM.md#L42`).

## Agent Workflow Checklist

1. Review open items in `0.0.4/Tasks-TODO/0.0.4-3-REVISIONS.md` before making edits.
2. Apply updates in a single focused branch per thematic change (terminology, schema, or algorithm).
3. Verify cross-file terminology alignment with `rg "^\*\*"` to scan dictionary blocks.
4. Request peer validation when altering the Continuity Spine or numeric determinism sections.
