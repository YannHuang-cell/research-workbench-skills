---
name: daily-paper-scout
description: Build a daily candidate reading list for the user from research themes, seed papers, authors, venues, and time windows without automatically writing anything into Zotero. Use when the user wants current, relevant, and reasonably authoritative literature suggestions, wants to track frontiers while keeping manual final selection, or wants a repeatable paper-scouting workflow for one or more research topics.
---

# Daily Paper Scout

Generate a daily shortlist, not a final bibliography.

- Treat this skill as a scouting workflow, not a reading workflow.
- Optimize for `coverage + frontier awareness + fit to the user's research`, not only for citation counts.
- Keep the user in the final selection loop.
- Do not automatically write results into Zotero.

## Inputs

- research themes or questions
- seed papers
- authors, groups, or venues to watch
- time window such as the last 3 months or last year
- optional preferences such as review papers first, code availability, or experimental relevance

## Core Workflow

1. Clarify the user's topic and what counts as relevant.
2. Build the search query set from themes, synonyms, seed papers, and known methods.
3. Search across multiple source types.
4. Merge and deduplicate candidates.
5. Score candidates by authority, frontier value, fit, and evidence support.
6. Output a short manual review list.

## Source Strategy

Do not rely on one source only.

- Use metadata-heavy sources for broad recall and filtering.
- Use recommendation-oriented sources for related-paper expansion.
- Use preprint sources for frontier awareness.
- Prefer official metadata or primary source pages when resolving bibliographic conflicts.

Use `references/source-strategy.md` for source roles and ranking logic.

## Ranking Logic

Score candidates along four dimensions.

### Authority
- review paper vs method paper vs tool paper
- venue reputation
- citation maturity when appropriate
- whether the work looks like a foundational anchor

### Frontier
- recent publication or preprint timing
- whether the work introduces a new method, benchmark, or task framing
- whether similar work is currently clustering around the same topic

### Fit
- topic match to the user's actual research questions
- overlap with the user's materials, modality, and method interests
- usefulness for near-term reading rather than abstract field awareness only

### Evidence
- visible code, data, supplementary material, benchmark participation, or strong experimental section

## Output Shape

Return a compact daily digest with sections such as:

1. 今日最值得看的 3-5 篇
2. Anchor papers
3. Frontier papers
4. Useful tools or benchmark papers
5. Why each item is here
6. What the user should screen manually next

Use `references/output-template.md` for the exact candidate format.

## Boundaries

- Do not pretend scouting equals understanding.
- Do not auto-import into Zotero.
- Do not over-weight preprints just because they are new.
- Do not over-weight citations just because they are high.
- Do not recommend papers without saying why they fit the user's topic.

## Hand-off

After the shortlist is produced:

- the user manually chooses what to keep,
- `read-paper-coach` handles deep reading,
- and `research-kb-builder` handles note deposition.
