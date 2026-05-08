# Research Workbench Skills

This repository organizes a multi-skill research workflow for a graduate student working across literature search, paper reading, code reading, programming growth, and Obsidian knowledge building.

The project is intentionally split into small, focused skills instead of one giant skill. The goal is to keep triggering clear, workflows stable, and outputs reusable.

## Repository Layout

- `skills/read-paper-coach`: Chinese paper-reading coach for one paper at a time.
- `skills/daily-paper-scout`: Daily literature scouting and candidate list generation.
- `skills/code-reading-coach`: Code-reading coach that adapts to the user's current level.
- `skills/coding-growth-coach`: Coding growth system for research programming and deeper CS study.
- `skills/research-kb-builder`: Obsidian knowledge-base builder for paper, code, concept, and idea notes.
- `skills/weekly-synthesis`: Weekly review and synthesis workflow.
- `docs/system-architecture.md`: System-level design, boundaries, and data flow.

## Current Status

- `read-paper-coach` is the first fully rewritten skill in this repo.
- The other skills are scaffolded with first-pass specs so the whole system can be reviewed as one repository.
- This repo is designed to be refined iteratively after real usage.

## Design Principles

- Keep `Zotero` as the literature fact layer.
- Keep `Obsidian` as the thinking and synthesis layer.
- Keep skills as workflow orchestrators instead of long-term databases.
- Avoid automatic writes to Zotero tags unless explicitly requested.
- Prefer structured Markdown outputs that can be pasted or written into Obsidian directly.

## Suggested Next Steps

1. Review `docs/system-architecture.md`.
2. Review `skills/read-paper-coach`.
3. Tighten the remaining skills based on real usage.
4. Initialize Git locally and push to GitHub from your machine.
