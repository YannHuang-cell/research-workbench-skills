# Modes

Use this file when choosing the right reading mode for the user's goal.

## Skim

Use when:
- the user is deciding whether to read the paper deeply,
- only a title, abstract, or first page is available,
- or the user wants a fast first-pass judgment.

Output:
- what problem the paper targets,
- what the high-level idea is,
- what evidence appears to support it,
- and whether it looks worth deeper reading for the user's purpose.

## Knowledge-Point Deep Read

Use when:
- the user wants to truly understand one paper,
- the paper is method-heavy,
- or the user wants checkpoint-based tutoring.

Output:
- one knowledge point at a time,
- one short recap,
- one short checkpoint question,
- and confirmation before advancing.

## Review Mode

Use when:
- the paper is a review or survey,
- the user explicitly wants paragraph-by-paragraph reading,
- or the citations themselves carry the main value.

Output:
- each paragraph block's role,
- the cited works that matter for that block,
- and how the paragraph fits the review's larger structure.

## Method Breakdown

Use when:
- the user asks what goes into the model and what comes out,
- the user asks about losses, modules, or inference,
- or the abstract explanation is not enough.

Output:
- input,
- modules,
- output,
- losses,
- train/infer difference,
- and why the design exists.

## Figure/Table/Formula Mode

Use when:
- the user points to one figure, one table, or one formula,
- or the main bottleneck is not the prose.

Output:
- what question the item is serving,
- how to read it,
- and the one conclusion to remember.

## Evidence QA

Use when:
- the user asks one focused question,
- the answer can be tied to one or two visible places in the paper,
- and a full tutoring loop would be unnecessary.

Output:
- direct answer,
- evidence anchor,
- uncertainty if the evidence is incomplete.

## Obsidian Output

Use when:
- the user wants the learning result written down,
- or the paper has been understood well enough to compress into a reusable note.

Output:
- structured Markdown using the templates in `obsidian-output.md`.

## Switching Rules

- `快一点` or `先概览`: switch toward `Skim`.
- `这里没懂`: stay in the same mode but lower the abstraction level.
- `这个方法到底怎么走`: switch to `Method Breakdown`.
- `这一段引用的都是什么`: switch to `Review Mode`.
- `只看图 3 / 表 2 / 这个公式`: switch to `Figure/Table/Formula Mode`.
- `整理成笔记`: switch to `Obsidian Output`.
