# Node Documentation — Outstanding Issues

Generated 11 Sep 2026 from a comparison of the live site
(https://polite-dune-0e6373c03.2.azurestaticapps.net/) against the local `dev`
branch preview (`mdbook serve`, http://localhost:3000).

**Scope note:** the TOC comparison found nothing on the live site that is missing
from `dev` — `dev` is a strict superset of `origin/main`. Everything below is a
defect present in `dev` (most of them inherited from `main`, i.e. currently live).

Paths are relative to `CreatorNodeDocumentation/` unless stated otherwise.

---

## 1. Broken internal links (4) — all currently live

All four are `.md` links that mdBook rewrites to `.html`, pointing at targets
that do not exist. None of them 404 during local review on Windows *except* by
inspection, because Windows is case-insensitive — the first one in particular
only fails once deployed to Azure (Linux).

| # | File | Line | Current link | Should be |
|---|------|------|--------------|-----------|
| 1.1 | `src/concepts/GeneralConcepts/assets.md` | 15 | `/concepts/GeneralConcepts/ImportExport.md` | `/concepts/GeneralConcepts/importExport.md` |
| 1.2 | `src/concepts/GeneralConcepts/node.md` | 83 | `/nodes/ExperssionParser/documentation.md` | `/nodes/ExpressionParser/documentation.md` |
| 1.3 | `src/concepts/GeneralConcepts/ephemeralState.md` | 9 | `/concepts/GeneralConcepts/subgraph.md` | `/concepts/GeneralConcepts/subgraphs.md` |
| 1.4 | `src/concepts/GeneralConcepts/destructive.md` | 9 | `/nodes/CombineMesh/documentation.md` | `/nodes/CombineMeshes/documentation.md` |

Note on 1.2: the visible link text is also misspelled — `[Experssion]` should
read `[**expression**]` (bold, per the node-name convention in
`DOCUMENTATION_PLAYBOOK.md`).

**Suggested guard:** add a link-check step to CI (e.g. `mdbook-linkcheck`, or
`lychee` over `book/`) so case and typo breakages fail the build instead of
reaching production.

---

## 2. Seven dead entries in the Deprecated section

`src/SUMMARY.md`, end of file. These entries have empty `()` targets, so mdBook
renders them as greyed-out, unclickable placeholder rows in the sidebar:

- `Create Material`
- `Set Material`
- `Apply Material`
- `Combine Meshes (V1)`
- `Extrude (V1)`
- `String Split (V1)`
- `Geometry Input (V1)`

Each carries an inline `<!-- TODO -->` comment. The comments do **not** leak into
the rendered HTML, but the empty nav rows do.

**Decide one of:**

- (a) write the missing `documentation.md` for each (preferred — `Deprecated`
  exists precisely so users landing on an old node find an explanation and a
  pointer to the V2), or
- (b) remove the entries from `SUMMARY.md` until their docs exist.

Do not ship them as empty rows.

For (a), each page needs at minimum: the one-line bold-italic summary, a
deprecation callout, and a link to the replacement node. Follow the template in
`DOCUMENTATION_PLAYBOOK.md`.

Special case: `Set Material` — the live Material node maps to the `SetMaterial`
folder, which is already published under **Geometry → Material & Texture →
Material**. Confirm whether a separate V1 page is actually wanted, or whether
this entry should just be dropped.

---

## 3. Two deploy workflows race on every push to `main`

Both trigger on `push: main`, both upload to the same Static Web App using the
same token, neither has a `paths` filter, and there is no ordering between them:

| Workflow | What it uploads |
|---|---|
| `.github/workflows/node-doc-cicd.yml` | Builds mdBook, uploads `CreatorNodeDocumentation/book` (`output_location: 'book'`, `skip_app_build: true`) — **this is the correct one** |
| `.github/workflows/azure-static-web-apps-polite-dune-0e6373c03.yml` | Uploads repo root with `output_location: ""` and no build step |

Whichever job finishes last wins the production deploy, so a push can
non-deterministically publish the wrong payload.

**Fix:** delete `azure-static-web-apps-polite-dune-0e6373c03.yml`, or reduce it
to its `close_pull_request_job` only. Verify first whether anything relies on its
PR-preview environments — if so, give it a build step and `output_location: book`
rather than leaving it uploading the raw repo.

---

## 4. Stray tracked file `src/#`

A 12-byte file containing `# Chapters`, tracked since Oct 2025, sitting in the
mdBook source root. Almost certainly the residue of a mistyped shell command.

**Fix:** `git rm 'CreatorNodeDocumentation/src/#'`

---

## 5. Typo on the Introduction page — currently live

`src/introduction.md` — "More information can be found in the Node **conecept**
section." Should be "concept".

---

## 6. Minor / housekeeping

- **`src/SUMMARY.md` has no trailing newline.** Last byte is `>`. Add one.
- **`theme/favicon.svg` differs from the deployed version** (2492 bytes local vs
  2452 on `main`). Intentional or accidental? Confirm before merge.
- **`NODE_DOCS_REVIEW.md`** (388 lines) is an internal working document that will
  land on `main` at merge. It sits outside `src/` so it will not publish to the
  site, but it will be public in the repo. Decide whether to keep it, move it, or
  drop it from the PR.

---

## 7. Not a bug — do not "fix" this

`.github/workflows/azure-static-web-apps-polite-dune-0e6373c03.yml` shows as a
~90-line diff between `origin/main` and `dev`. It is **purely CRLF → LF
normalisation** — equal insertions and deletions, zero content change. This is
the exact case documented under "Line endings" in the repo's root `CLAUDE.md`.
Leave it alone and do not let a reviewer chase it.

(If item 3 is actioned, this file is deleted anyway and the point is moot.)

---

## Verification checklist

After fixes:

1. `cd CreatorNodeDocumentation && mdbook build` — completes with no warnings.
2. Every link in section 1 resolves (check the built `book/` output, not just the
   source, and check with case sensitivity in mind).
3. No empty `()` entries remain in `src/SUMMARY.md`, or the ones that remain are
   a deliberate, documented decision.
4. `git diff --stat origin/main..HEAD -- .github` reflects only intended changes.
