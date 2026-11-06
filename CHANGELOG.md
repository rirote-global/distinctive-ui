# Changelog

## 1.2.1 — 2026-11-07

- **Setup gate.** A missing helper could be detected and then never offered (a homepage request ran
  without ever offering scroll-craft). `check-helpers.mjs` now takes `--page landing|product` and prints
  `offerNow`, the exact offers owed, plus a `gate` line. The skill must put those offers in its first
  reply, alongside Round A; sending Round A without them counts as a workflow failure. Product UI never
  gets the scroll-craft offer.
- **Handover names the helpers.** The handover template gains a "Helpers" line that says whether
  scroll-craft led, was declined or was never offered, so a skipped offer surfaces at the end at the latest.

## 1.2.0 — 2026-11-06

- **Build log.** New `references/build-log.md`: a per-person log of shipped looks
  (`~/.claude/distinctive-ui/BUILDS.md` by default). Phase 3 directions must differ from every row on
  at least 3 of 5 dimensions; Phase 6 appends the shipped direction. Stops client projects drifting
  into one house style. An empty log is backfilled with the user's already-shipped looks before the
  first gate, so the check works from the first project.
- **Hard rules.** `references/directions.md` gains a Never / Instead table of ship-blockers, each with
  its fix, run alongside the anti-template checklist in Phase 4.
- **scroll-craft routing.** Scroll-driven landing pages and marketing sites are handed to
  `scroll-craft` (optional, third-party, github.com/nateherkai/scroll-craft) when it is installed,
  after this skill's intake. Product UI always stays here. `check-helpers.mjs`, `design-orchestrator`
  and `/distinctive-ui:setup` detect and offer it like the other helpers.

## 1.1.0 — 2026-10-22

- Helper skills are no longer hard dependencies. `ui-ux-pro-max` and `apple-design` are detected first
  (personal skills folder, project, installed plugins, session skill list) and offered for install only
  when missing, so nobody gets duplicate copies, and any helper can be removed without breaking the plugin.
- New `scripts/check-helpers.mjs` (read-only detection), used by the main skill and `/distinctive-ui:setup`.
- README and setup rewritten to match.

## 1.0.0 — 2026-10-22

- First release: `distinctive-ui` workflow (intake → brief → three directions → build → browser review → handover).
- Bundled `design-orchestrator` routing between ui-ux-pro-max and apple-design, with fallback rules when either is missing.
- `/distinctive-ui:setup` checks and installs helper skills and tools, asking first.
- `scripts/shoot.mjs`: dependency-free headless-Chrome screenshots and flow tests.
