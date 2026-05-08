# System Architecture

This repository models the research workflow as a set of cooperating skills rather than a single all-purpose skill.

## Core Roles

### Zotero
- Store papers, PDFs, metadata, and annotations.
- Remain the source of truth for bibliographic facts.
- Do not receive automatic tag writes by default.

### Obsidian
- Store literature notes, concept notes, method notes, code notes, project notes, and idea notes.
- Act as the durable second brain.
- Prefer object-based notes and relationship fields over heavy folder nesting.

### Skills
- Handle task-specific workflows.
- Produce structured outputs.
- Help the user move from raw input to understanding, synthesis, and action.

## Skill Map

### 1. Daily Paper Scout
- Input: themes, seed papers, authors, venues, time window.
- Output: candidate reading list for manual review.
- Does not write directly into Zotero.

### 2. Read Paper Coach
- Input: one paper or one paper fragment.
- Output: understanding, evidence-backed explanations, and optionally an Obsidian-ready note.

### 3. Code Reading Coach
- Input: notebook, script, or repository.
- Output: entry points, call flow, data flow, key modules, and suggested practice edits.

### 4. Coding Growth Coach
- Input: current level, study goals, current project needs.
- Output: staged study plan, exercises, and review loop.

### 5. Research KB Builder
- Input: completed reading, code understanding, project insight, or idea.
- Output: structured Obsidian notes that fit the same vault system.

### 6. Weekly Synthesis
- Input: the week's papers, code, notes, and ideas.
- Output: concise synthesis, open questions, next actions, and review targets.

## Data Flow

1. `daily-paper-scout` produces a shortlist.
2. The user manually selects what enters Zotero.
3. `read-paper-coach` helps the user understand one item deeply.
4. `research-kb-builder` turns that understanding into Obsidian notes.
5. `code-reading-coach` and `coding-growth-coach` support implementation and skill growth.
6. `weekly-synthesis` pulls the week's work together and feeds new directions back into future search and reading.

## Why This Split

- Search, reading, coding, and note building have different success criteria.
- A giant skill would be harder to trigger correctly and harder to maintain.
- This split keeps each skill narrow while still enabling a coherent end-to-end workflow.
