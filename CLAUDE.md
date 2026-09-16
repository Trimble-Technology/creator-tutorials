# creator-tutorials

## What this repo is

This repo holds the **content that powers learning material for Trimble Creator** — the node-based/graph procedural modeling tool inside SketchUp (also referred to as "Materia" graphs in the underlying schema). It has two independent halves:

1. **In-app tutorials** (`tutorials/`) — the step-by-step graph tutorials shown inside the Creator app itself (intro walkthroughs, patterns, and full "build" projects).
2. **Node documentation site** (`CreatorNodeDocumentation/`) — the public reference site documenting every node in Creator, built with [mdBook](https://rust-lang.github.io/mdBook/) and deployed to Azure Static Web Apps.

Both are content repos, not application code — most files are Markdown and JSON. The Creator app and the docs site both pull their content directly from this repo (via raw GitHub URLs and a build pipeline, respectively), so **what's merged to `main` is what's live**.

## Branching model

- **`dev`** is the working branch. Do content work here.
- **`main`** is production. Merging `dev` → `main` (via PR) is what:
  - Publishes tutorials to the live Creator app (see "How tutorials reach the app" below).
  - Triggers the GitHub Action that rebuilds and redeploys the node documentation site.
- Don't edit `main` directly — go through `dev` and a PR.

## Repo structure

```
tutorials/
  tutorials.json                  # master list of "featured" tutorials shown in-app (raw GitHub URLs, must point at `main`)
  graph/
    intro/          # first-time-user walkthroughs (navigation, node interactions, connections, etc.)
    pattern/        # short, focused "how do I do X" graphs
    builds/         # full example projects (may include .trb Creator project files alongside the write-up)
    examples/
      featured-graphs.json   # master list of featured example graphs (same raw-URL pattern)

CreatorNodeDocumentation/
  src/              # SOURCE OF TRUTH — edit here
    nodes/<NodeName>/
      descriptor.json     # machine-readable node definition (inputs/outputs/type/path in the node picker)
      documentation.md     # human-readable node reference page
    concepts/         # conceptual/reference pages (Graph, Node, Connection, Asset, etc.)
    SUMMARY.md        # mdBook table of contents — MUST be updated by hand when a page is added/removed/moved
  theme/              # site styling (custom.css, favicon)
  book/               # BUILD OUTPUT — never hand-edit, it's regenerated and overwritten on every deploy
  book.toml           # mdBook config (title, theme, search settings)

.github/workflows/    # CI: builds mdBook and deploys to Azure Static Web Apps on push to `main`
```

## Tutorial content format

Each tutorial is a matched pair of files, named by a UUID, living together in a folder under `tutorials/graph/<intro|pattern|builds>/<tutorial-name>/`:

- **`<uuid>.md`** — the tutorial body text shown to the user.
- **`<uuid>.json`** — metadata describing the tutorial, in this shape:

```json
{
  "header": {
    "assetSchemaVersion": 1,
    "contentSchemaVersion": 1,
    "assetType": "tutorial:materia:graph"
  },
  "content": {
    "id": "<same uuid>",
    "name": "Tutorial Title",
    "text": "https://raw.githubusercontent.com/Trimble-Technology/creator-tutorials/main/tutorials/graph/.../<uuid>.md",
    "tags": [null],
    "tutorialType": "pattern",
    "actions": [
      { "type": "loadMateriaGraph", "arguments": { "uri": "whp:<graph-asset-id>" } }
    ]
  }
}
```

Notes:
- The `text` field is a **raw GitHub URL pointing at `main`** — this is why a tutorial isn't live until its branch is merged to `main`.
- `tutorialType` matches its parent folder (`intro`, `pattern`, or `builds`).
- Some `builds/` tutorials also ship a `.trb` file (the actual Creator project) alongside the `.md`/`.json` pair.

### How tutorials reach the app
`tutorials/tutorials.json` and `tutorials/graph/examples/featured-graphs.json` are flat lists of raw-GitHub-URL pointers to individual tutorial/graph JSON files. Adding a new tutorial means: (1) add the `.md`/`.json` pair in the right folder, and (2) add its raw URL to the relevant list file, if it should be "featured."

## Writing style guide (from the root `README.md`)

When writing tutorial or node-doc text, use:

| Format | For |
|---|---|
| **bold** | node names/types |
| *italic* | xput (input/output) names |
| ALL CAPS | keyboard actions |
| Capitalized-lowercase (e.g. "CTRL-click") | mouse actions |
| [square brackets] | values to type or select |
| "quotes" | names of things (a renamed node, glossary terms) |
| 'apostrophes' | vague/informal descriptions (e.g. 'glow') |

Naming conventions:
- Tutorial names: Title Case.
- Step names: Sentence case.

Glossary: "Graph viewer" = the panel showing the graph/nodes; "3D viewer" = the panel showing 3D geometry; "NURBS" is always all-caps.

## Node documentation conventions

Each node's `documentation.md` follows a consistent template: a one-line **bold italic** summary, then `#### Inputs` and `#### Outputs` sections (each xput as an italic bullet with an indented description), then optional `### Note(s)` and `### Example(s)` sections. Example links point to `creator.trimble.com/graph?assetURI=...` so a reader can open the live example graph.

**For the full rulebook — exact template, spacing rules, the `geometry` bold-italic convention, deprecation callouts, `SUMMARY.md` wiring, and a pre-commit checklist — see `CreatorNodeDocumentation/DOCUMENTATION_PLAYBOOK.md`.** Follow it whenever writing a new or missing `documentation.md`.

`descriptor.json` is the technical definition consumed by the app's node picker (name, path/category, inputs/outputs with types, node class) — keep it in sync with what `documentation.md` describes.

## Building/previewing the docs site locally

```
cd CreatorNodeDocumentation
mdbook serve
```
Then open http://localhost:3000. (Requires the mdBook CLI — see the install link in `CreatorNodeDocumentation/README.md`.) Never hand-edit anything under `CreatorNodeDocumentation/book/` — it's fully regenerated on every build.

## Line endings

This repo is normalized to LF (`.gitattributes` → `* text=auto eol=lf`). If a large number of files ever show as "modified" with no real content change, it's almost certainly a line-ending mismatch, not real edits — check with `git diff --stat` (equal insertions/deletions across many files is the tell) before assuming real changes were made.
