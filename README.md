# Rive | decision intelligence platform

A single-file, self-contained prototype of the Rive decision intelligence and
orchestration platform, built around a cold chain use case. No build step, no
dependencies, no server: open the HTML and the whole app runs in the browser.

**Live:** https://arunk-rgb.github.io/rivedesign/

## What is in it

The launcher on Home groups every app the platform ships with. The ones with
working screens are:

| App | What it does |
| --- | --- |
| **Cold Chain Intelligence** | The landing dashboard: KPI strip, network conditions, and the Allocator, Cold Chain Monitor and Custodian agents with their priority actions. Drills into agent detail, a recommendation panel, the knowledge graph and the Orchestra copilot. |
| **Lanes, Sales Orders, Shipments, Assets, Products, Batches** | The operational registers, each a wide sortable table with its own detail view. |
| **Work Orders, Documents, Measurements** | Maintenance and evidence records. |
| **Agents** | The agent catalogue, jobs and schedules. |
| **Integrations** | Six external systems as Workato-style projects, with recipes, connections, lookup tables, deployments, version history, job logs and a recipe editor. Styled on the Palantir Blueprint design system. |
| **Ontology** | 23 object types on a pan-and-zoom ERD canvas plus a Business Object Studio table. Selecting a type shows its properties, links, backing datasource and object actions. |

## Two things worth knowing

**Integrations and Ontology are joined up.** Every object type in the Ontology
names the system that backs it and the exact recipe that feeds it, and
*Open in Integrations* jumps straight to that project. Shipment lands on
project44's `01 · project44 → Rive · Shipment Position · Stream`.

**The Ontology mirrors the app's real data.** Each object type carries the
attributes the app actually holds, taken from the columns on its list view, so
Lane has all 25 of its real fields rather than a plausible-looking subset.

## Themes

Light and dark both work throughout. Personalization (avatar menu, bottom left)
carries eleven brand colours and live theme previews; the default is near-black.
Integrations deliberately stays on Blueprint blue rather than following the brand
switcher, because that is Blueprint's own intent system.

## Files

- `index.html` — served by GitHub Pages
- `Rive-decision-intelligence-platform.html` — the same file under its real name

They are byte-identical. Git stores one blob for both, but an edit needs
applying to both copies to keep them in step.

## Known gaps

- `source-doc-page.jpg` 404s. It is a local asset that was never in the source
  file, so one document-preview thumbnail is blank. Pre-existing, cosmetic.
- The recipe editor renders and navigates but does not support adding or
  reordering steps.
