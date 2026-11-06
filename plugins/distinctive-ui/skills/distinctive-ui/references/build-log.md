# The build log

Three directions per project stop one screen from looking like a template. They do not stop
**your** projects from slowly converging on one house look: the same ledger rules, the same mono
numbers, the same paper-and-ink palette, client after client. The build log is the memory that
catches that. It records what has shipped, so the next project has to be different from it.

## Where it lives

Resolved, never assumed. First hit wins:

1. `$DISTINCTIVE_UI_LOG` (a file path)
2. `<project root>/.claude/distinctive-ui/BUILDS.md`, if the project already has one
3. `~/.claude/distinctive-ui/BUILDS.md` (the default: one log per person, across all projects)

If the file does not exist, create it with the header row below and say so in one line. An empty log
has nothing to clear: the first build passes by definition.

## Row format

One row per **shipped or approved** direction. Not the two that lost.

```markdown
| Date | Project | Composition | Navigation / chrome | Palette family | Type pairing | Signature interaction |
|---|---|---|---|---|---|---|
| 2026-10-29 | riroteglobal.com | Document: audit report | Top bar + mobile sticky CTA | Report paper, ink, finding red | IBM Plex Sans + Plex Mono | Symptom checklist pre-fills the contact form |
```

What each dimension records:

| Dimension | Record | Counts as different when |
|---|---|---|
| Composition | The layout family from the layout-from-job table in `directions.md` (work queue, document, ledger, timeline, split, one-action field screen…), or the scroll-craft grammar | It is another family, not the same family re-spaced |
| Navigation / chrome | What the chrome is and what it is for (sidebar, top bar, tab strip, divider, folio, none) | The visitor finds their way in a different way |
| Palette family | The material metaphor and its 2–3 core hues | Another material, not the same one recoloured |
| Type pairing | Both faces | At least one face changes and its role changes |
| Signature interaction | The one bespoke interaction, in a phrase | Always different: it is bespoke by definition |

## The gate

Each of the three directions in Phase 3 must differ from **every** existing row on **at least 3 of
the 5** dimensions, checked against each row on its own, not on average. Because the signature
interaction always differs, this really asks for two more out of the other four.

- Check before writing the directions up, not after.
- A direction that fails gets changed. **Never edit an old row to make a new direction pass.** The log
  is a record of what exists, not of what you wish existed.
- The user can overrule the gate (a client who wants their sister brand to match). Then record it as
  an ASSUMPTION in the brief, and note "gate waived by user" in the new row.
- Under the trade-off table, one line: `Build log: clears all N rows` or `fails row <date> on <dims>`.

## After handover

Append one row for what shipped. In the handover, say which dimensions it shares with earlier rows,
because those shared columns are what the next project has to avoid.

For a build that scroll-craft led, add the row here too (its grammar goes under Composition), so one
log covers everything you ship. scroll-craft keeps its own `FINGERPRINTS.md` as well; do not merge them.
