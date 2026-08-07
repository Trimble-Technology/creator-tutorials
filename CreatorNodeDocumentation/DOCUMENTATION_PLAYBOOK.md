# Node Documentation Playbook

How to write a `documentation.md` file for a node in `CreatorNodeDocumentation/src/nodes/<NodeName>/`. This was reverse-engineered by analyzing all 174 existing `documentation.md` files for consistent patterns — where files disagreed, the majority convention was chosen. Follow this exactly for new or missing node docs so the reference site stays consistent.

This complements (doesn't replace) the general writing style guide in the root `README.md` ("Tutorial Guidelines") — bold/italic/caps rules there apply here too.

## Before you start

- Find (or create) the node's `descriptor.json` in the same folder — it's your source of truth for exact xput names (`displayName`), the node's `type` identifier, and `alternateNames`. The prose you write must match it exactly (see "Keep it in sync with descriptor.json" below).
- If you're not sure whether a doc already exists, check `CreatorNodeDocumentation/src/SUMMARY.md` for the node — if its entry is an empty link `[Name]()`, the page doesn't exist yet and you're filling a gap.

## The template

Copy this and fill in the blanks. Line-for-line spacing matters (see "Exact spacing rules" below) — mdBook/CommonMark needs blank lines around list items or they won't render as a list.

```markdown
# Title Case Node Name

**_One-sentence description of what the node does, ending in a period._**

---


#### Inputs

* _input name_

  * Description of the input.

* _second input name_

  * Description of the second input.


#### Outputs

* _output name_

  * Description of the output.


### Note(s)

* Any caveats, gotchas, or behavior worth calling out.

* Other names for this node include: X, Y, and Z.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:<uuid>&version=latest" target="_blank">Example graph title</a>
```

`Note(s)` and `Example(s)` are optional — skip a section entirely if you have nothing to put there (don't leave an empty heading). Everything else (title, summary, divider, Inputs, Outputs) is required.

## Section-by-section rules

**Title (`# `)** — Title Case, matches the node's display name (the human-readable name, not the internal `type` field or the camelCase key). E.g. descriptor `"name": "absolute value"` → `# Absolute value`.

**Summary line** — always wrapped in bold+italic: `**_Does the thing._**`. One sentence, ends with a period. This is the only place a full sentence gets the bold-italic treatment — everywhere else, bold-italic is reserved for the `geometry` xput (see below).

**Divider** — a literal `---` on its own line, always present, always right after the summary.

**Deprecation callout (only if applicable)** — if a node is deprecated/superseded, add a blockquote directly after the `---` (one blank line before it, two blank lines after before `#### Inputs`):

```markdown
> #### DEPRECATED
>
> Why it's deprecated / what's wrong with it.
>
> Superseded by [New Node Name](/nodes/NewNodeName/documentation.md)
```

(Note: the one existing example of this in the repo, `Circle/documentation.md`, has this section title as "DEPRICATED" and says "Superseeded" — both are typos. Use the correct spellings above for anything new; don't copy the typo.)

**Inputs / Outputs (`#### `)** — heading level 4, exactly `#### Inputs` and `#### Outputs` (this is the dominant convention — 170/174 files use it; a handful of very old files use `### Inputs` at level 3 or "Inputs"/"Outputs" without the "#### " — don't follow those).

Each xput is a bullet with its name in italics, followed by a blank line, then an indented (2-space) bullet with the description:

```markdown
* _xput name_

  * What it does / what it means.
```

If an xput accepts multiple values or needs more explanation, you can add further indented detail as a nested bullet directly under the description line (no blank line before it, indented one more level — 4 spaces total):

```markdown
* _type_

  * Sets the type of circle to output. These are `NURBS curve`, `polyline`, and `mesh`.
    * Adjusting the _start angle_ and _end angle_ inputs will create an arc/semicircle.
```

**The one exception to plain italics — `geometry`.** Whenever the xput being described is literally named "geometry" (the node's core primitive input/output), bold it as well: `**_geometry_**`. This is a deliberate, 100%-consistent convention across the whole doc set to flag the "main" data flowing through the node. No other xput name gets this treatment, regardless of how central it is to the node.

**Connection cardinality.** For geometry inputs specifically, say whether the node accepts one connection or many, e.g.:
- `Accepts a single geometry connection (unless the SHIFT key is held).`
- `Accepts multiple geometry connections.`

**Point-list outputs.** If a node outputs geometry, it's conventional to also expose the flattened point data as sibling outputs using dot notation, each with its own bullet:

```markdown
* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.
```

**Singular + list output pairs.** Math/value nodes commonly expose both a single result and a list form, described as a pair:

```markdown
* _result_

  * The result of addition.

* _result list_

  * The list of results of addition.
```

**Note(s) (`### `)** — heading level 3, `### Note(s)` (not "Notes" — that's a legacy variant found in ~36 older files, don't use it for new docs). Use for caveats, edge cases, performance notes, or anything a user would trip over. Two conventions worth reusing:

- If the node corresponds to an operator/function in the [**Expression**](/nodes/ExpressionParser/documentation.md) node, say so: `This operation is represented as \`+\` within the [**Expression**](/nodes/ExpressionParser/documentation.md) node.`
- Nearly every node ends its Note(s) with an "other names" bullet (165/174 files do this) — see the dedicated rule below.

**"Other names for this node include" bullet.** Pull this directly from `descriptor.json`:
- If `alternateNames` is non-empty, list them Title Case (except literal symbols like `+`), comma-separated with "and" before the last: `Other names for this node include: Sum, Addition, +, and plus.`
- If `alternateNames` is empty, fall back to the node's internal `type` identifier if it reads as a recognizable alias: `Other names for this node include: Abs.`
- If there's truly nothing else to call it, omit this bullet.

**Example(s) (`### `)** — heading level 3, `### Example(s)` (same rule as Notes — not "Examples"). Every example is an HTML anchor tag, not a markdown link — this is 100% consistent across every example in the repo (249/249):

```markdown
* <a href="https://creator.trimble.com/graph?assetURI=whp:<uuid>&version=latest" target="_blank">Descriptive title</a>
```

Get the `assetURI` UUID from the actual example graph in Creator; the title is a short human-readable label for what the example demonstrates (not necessarily the node name).

## Formatting rules (applies throughout)

- Bullets always use `*`, never `-`.
- Blank line between the section heading and its first bullet.
- Blank line between every bullet item (both top-level and the xput-name → description pairs).
- **Two** blank lines between major sections (after `---`, and between Inputs/Outputs/Note(s)/Example(s)) — one blank line reads as "still part of the same block" to mdBook; two cleanly separates sections. This is easy to get wrong by eye — check against an existing file if unsure.
- *Italic* — xput names (`_value_`), matching the root style guide's "xput names" rule.
- **Bold** + italic — reserved for the one-sentence summary at the top, and for `**_geometry_**` xputs specifically.
- `Code ticks` — literal values a user would type or see verbatim: `true`, `false`, `0`, enum choice strings like `NURBS curve` or `CSG`, or expression syntax like `abs()`.
- ALL CAPS — keyboard actions (`SHIFT`, `CTRL`), per the root style guide.
- Internal links to other node docs: `[**Node Display Name**](/nodes/NodeFolderName/documentation.md)` — bold the link text, use the node's display name (not its folder/type name) as the link text, and use an absolute path starting with `/nodes/`.
- Internal links to concept pages follow the same pattern: `[**Concept Name**](/concepts/GeneralConcepts/fileName.md)`.
- No images are currently used in any node doc — text and the linked example graphs carry the explanation. If you think an image is genuinely needed, raise it rather than introducing the first one unilaterally.

## Keep it in sync with `descriptor.json`

Before you consider a doc finished, cross-check it against the node's `descriptor.json` in the same folder:

- Every key in `descriptor.json`'s `input` and `output` objects should have a matching xput bullet, named using the JSON's `displayName` (not the camelCase key).
- The doc shouldn't document xputs that don't exist in the descriptor, or vice versa.
- If the descriptor changes (an xput renamed, added, or removed), the doc needs a matching update in the same change.

## Adding the page to the site

A `documentation.md` file sitting in its node folder isn't enough on its own — it has to be wired into `CreatorNodeDocumentation/src/SUMMARY.md` or it won't appear in the sidebar/build at all:

1. Find the node's category in `SUMMARY.md` (or the "Missing (needs to be classified)" section if you're not sure where it belongs yet).
2. Turn its empty placeholder link into a real one: `- [Display Name]()` → `- [Display Name](nodes/NodeFolderName/documentation.md)`.
3. **Check for duplicates before you commit** — the same target file can only appear once anywhere in `SUMMARY.md`, or `mdbook build`/`mdbook serve` will fail outright with a "Duplicate file in SUMMARY.md" error (this happened once already — see the "Fix duplicate SUMMARY.md entry" commit). If a node has multiple SUMMARY.md entries (e.g. a current version and a "(V1)" deprecated one), each needs its *own* `documentation.md` file — don't point two entries at the same file.
4. Preview locally with `mdbook serve` (see `CreatorNodeDocumentation/README.md`) before pushing, to confirm the page builds and renders.

## Quick checklist

- [ ] Title is Title Case and matches the descriptor's display name
- [ ] One-sentence bold-italic summary, ending in a period
- [ ] `---` divider
- [ ] Deprecation callout added, correctly spelled, if applicable
- [ ] `#### Inputs` and `#### Outputs` — every xput from `descriptor.json` covered, named via `displayName`
- [ ] `geometry` xputs (and only those) are bold+italic
- [ ] `### Note(s)` / `### Example(s)` — present only if there's real content, correct "(s)" heading
- [ ] "Other names" bullet pulled from `alternateNames` / `type`, if applicable
- [ ] Examples use the `<a href="..." target="_blank">` anchor format, not markdown links
- [ ] Blank-line spacing matches the rules above (2 blank lines between sections)
- [ ] `SUMMARY.md` entry updated to point at the new file, and checked for duplicates
- [ ] Previewed with `mdbook serve` before pushing
