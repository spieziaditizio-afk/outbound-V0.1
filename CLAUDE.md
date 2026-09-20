# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single self-contained HTML file — `Outbound Control Tower - DEMO.html` — simulating a warehouse outbound delivery board for the Special Operations Area, Sevenum. No build step, no package manager, no server, no dependencies. All CSS and JS live inline in that one file. The image files in the repo root (`EPT*.jpg`, `VNA*.jpg/webp`, `cawila*.png`, `precision*.png/webp`, `Mooffz.png`, `pick label.jpg`) are reference photos for the physical cone markers — the app does not load them at runtime.

## Commands

There is no build, lint, or test tooling — this is a static file.

- Open `Outbound Control Tower - DEMO.html` directly in a browser (double-click or `file://`) to test changes.
- Use the in-app "Reset demo data" button (Activity view) to replay `SEED` and return to a clean starting shift after breaking state.
- Use the "Second screen" button to open a second window and exercise the cross-tab sync path.

## Architecture

Everything lives in one `<script>` block, organized into 19 numbered sections (search for the `N. SECTION NAME` banner comments):

- **1. Reference data** — `COLOR_HEX`/`COLOR_NAME`, `STOCK` (physical cone/disc/hex counts on the rack), `STATUSES` (the fixed pipeline), `ROLES` (which statuses each role may move a delivery into), `USERS` (demo login accounts with PINs).
- **2. Countries and flags** — flags are hand-drawn inline SVG, not emoji (Windows does not render flag emoji reliably), keyed by `COUNTRY_BY_CODE`.
- **3. Marker drawing** — a "marker" is a traffic cone, optionally topped with a colored disc or hex saucer. `markerSVG`/`markerName`/`markerShort` render it at different sizes and verbosity.
- **5. State** — one global `state` object (`{deliveries, log, lost, seeded}`) persisted to `localStorage` under `oct.demo.state.v1`; `save()` writes it and broadcasts it.
  - **Live sync** (same section): three fallback transports keep multiple open windows in sync — `BroadcastChannel` (same origin), a `window.opener`/child-window `postMessage` mesh (`relays()`/`send()`/`handle()`), and the `storage` event as last resort. Every message carries the full state, so no transport depends on `localStorage` actually being writable. Read `initSync()`, `handle()`, and `broadcast()` together before touching sync behavior — it's the trickiest part of the file.
- **7. Allocation engine** (`allocate`/`candidates`) — assigns a marker to a new delivery. Priority order: never reuse a marker a live delivery already holds; prefer a plain cone over a cone+topper combo; best-fit the smallest color pool that still covers the pallet count (keeps deep pools free for bigger deliveries); when a combo is needed, avoid `CONFUSABLE` color pairs and spread topper usage evenly across the `disc`/`hex` shapes.
- **8. Mutations** — `createDelivery`, `moveDelivery` (gated by `canMove`/`ROLES.move`), `returnCones` (releases a marker back to stock, writes off whatever didn't come back). Every mutation calls `logEvent` then `save()`.
- **9. Seed** — `SEED` + `seed()` build a believable starting shift by replaying real `createDelivery`/status-transition calls rather than hand-crafting state, so seeded data stays consistent with what the allocation engine and history log would actually produce.
- **10–16. Render** — `renderAll()` fans out to one render function per view (board, drawer, cone stock, returns, activity log). Render functions are pure functions of `state` + `me` (the signed-in user) and rebuild `innerHTML` from scratch — no framework, no diffing.
- **17–19. Login, navigation/TV mode, boot** — PIN-based demo login (`USERS`); `data-mode="tv"` on `<html>` drives a wall-monitor CSS variant; `@media print` limits printing to the assignment ticket only.

### Delivery status pipeline

`STATUSES` plus two out-of-band statuses (`loaded`, `closed`) that live outside the board lanes:

```text
allocated → picking → pick_dropped → packing → strap → next_day|today → loaded → closed
```

A delivery's `marker` is reserved from `STOCK` the moment it's created via `createDelivery`, and isn't released until `returnCones` closes it. `reservations()`/`freeOf()` compute live stock pressure from every non-`closed` delivery, including ones already `loaded`, not just what's visible on the board.

## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

Rules:
- For codebase questions, first run `graphify query "<question>"` when graphify-out/graph.json exists. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
