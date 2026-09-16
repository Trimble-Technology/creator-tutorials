# Creator node documentation — full review

**Date:** 2026-09-09
**Scope:** all 177 node folders in `CreatorNodeDocumentation/src/nodes/`, plus `SUMMARY.md` and internal/example links.
**Method:** every `documentation.md` was read in full and cross-checked against its `descriptor.json`, plus scripted checks for xput coverage, enum options, alternate names, headings, links, and example URLs.

---

## 0. Important caveat about the comparison source

The `materia-creator` folder **does not contain any node definition data**. The whole tree (701 files, all branches, git history) was searched — no node names, no descriptors, no node metadata. It's the web app shell only.

The authoritative node definitions come from an npm package that repo depends on:

```
@materia/node-descriptors  @ 32.3.16
https://artifactory.trimble.tools/artifactory/api/npm/CDG-npm/@materia/node-descriptors/-/...
```

There is no `node_modules` in the checkout and unauthenticated requests to artifactory return 403, so **this review compares `documentation.md` against the `descriptor.json` files checked into `creator-tutorials`** — not against the live engine.

That matters because the `descriptor.json` copies in this repo may themselves be stale. Everything in §5 below is a suspected descriptor-side problem, and every "missing input" finding could in principle be the opposite (a descriptor that's ahead of, or behind, the engine). **Recommended next step:** install `@materia/node-descriptors@32.3.16` (or newer) once and diff all 177 descriptors against it. That is the only way to be sure the docs and the app agree.

---

## 1. Summary

| Category | Count |
|---|---|
| Node folders | 177 |
| `documentation.md` present | 177 |
| `descriptor.json` present | 175 (+2 misnamed `description.json`) |
| **Inputs/outputs in descriptor but not documented** | **74, across 29 nodes** |
| **Inputs/outputs documented but not in descriptor** | **35, across 29 nodes** |
| Descriptions that are factually wrong or copy-pasted from another node | 24 |
| Headings that will not render (indented) | 2 |
| Broken / non-canonical example links | 11 |
| Broken internal link | 1 |
| Placeholder / staging URLs published live | 5 |
| Doc title ≠ descriptor display name | 7 |
| `alternateNames` not reflected in "Other names" bullet | 29 |
| Enum options never mentioned in the doc | 8 |
| Playbook style deviations | ~200 |
| Suspected descriptor-side bugs (engineering) | 21 |

Nothing found breaks `mdbook build`. `SUMMARY.md` has no duplicate targets and every node folder is linked, so no page is orphaned.

---

## 2. P1 — Fix first

These either misinform the reader outright, hide real functionality, or render incorrectly.

### 2.1 `GetAttribute` — the doc is a copy of `AddAttribute` and describes the wrong node

This is the single worst page in the set. `Get attribute` reads attributes; the doc describes writing them.

- Documents `_type_`, `_attribute name_`, `_value_` with **AddAttribute's** wording ("Sets the type of attribute **to add**", "The name **to give** the attribute", "The value **to assign** to the attribute").
- **Missing every real input:** `mode` (per point / per primitive / on node / on graph), `type` (attributeType), and the three `default` inputs (`defaultValue`, `defaultVectorValue`, `defaultStringValue`).
- **Missing every real output:** `number`, `vector`, `string`, `number list`, `vector list`, `string list`.
- **Documents six outputs that don't exist:** `points`, `points.x`, `points.y`, `points.z` (and an `_value_` input).

Needs a full rewrite from the descriptor.

### 2.2 `And` and `Or` — all four inputs are labelled `_value 1_`

Both files list the input name `_value 1_` four times while the descriptions correctly read "first / second / third / fourth value to check". Should be `_value 1_` … `_value 4_`.

### 2.3 Switch nodes — documented xput names don't match the app at all

| Node | Doc says | Descriptor says |
|---|---|---|
| `FloatSwitch` (Number switch) | outputs `_result_`, `_result list_` | `value`, `value as list` |
| `StringSwitch` | inputs `_value 0_`–`_value 3_`; outputs `_result_`, `_result list_` | inputs `string 1`–`string 4`; outputs `string`, `string list` |
| `VectorSwitch` | inputs `_value 0_`–`_value 3_`; outputs `_result_`, `_result list_` | inputs `vector 0`–`vector 3`; outputs `vector`, `x`, `y`, `z`, `vector list`, `x list`, `y list`, `z list` |

`VectorSwitch` is missing **six** real outputs. Note also that `StringSwitch`'s descriptor keys are `string0`–`string3` while its display names are `string 1`–`string 4` — the index input is 0-based but the labels are 1-based (see §5).

### 2.4 Two nodes have no `descriptor.json` — the file is misnamed `description.json`

- `ExtractUV/description.json`
- `FlipUV/description.json`

Rename both to `descriptor.json`. Anything that reads descriptors by filename (the node picker sync, the playbook's cross-check step) currently skips these two nodes silently.

While there: **`ExtractUV` is missing its `geometry` input** entirely, and the descriptor's `help` ("Gets UVs from **surface** points") contradicts the doc, which says the node only works on PolyMesh and *not* on NURBS surfaces.

### 2.5 Descriptions copied from the wrong node (factually wrong)

| Node | Xput | Doc says | Should describe |
|---|---|---|---|
| `Locator` | `_type_` | "the **position** of the locator" | the semantic type string (`{"type": "snap"}`) |
| `Magnitude` | `_vector_` | "The vector value **to subtract from**" | the vector to measure |
| `SubtractVectors` | `_result_`, `_result list_` | "The **normalized** vector" / "list of results of **normalized** vectors" | the subtraction result |
| `SetVectorListItems` | summary | "Sets multiple item values in a **number** list" | vector list |
| `FloatValue` (Number) | `_value_` output | "The **integer** value…" | number / floating point value |
| `TesselatePatch` | `_qualityV_` | "quality for the **U** coordinate" | V coordinate |
| `AddVectors`, `AddVectorsV2` | `_vector 2_`, `_vector 3_`, `_vector 4_` | all three say "The **first** vector value for addition" | second / third / fourth |
| `PolyBox` (Box) | `_uniform scale_` | "The **vector** value…" | it's a single float |
| `Tetrahedron`, `TetrahedronV2` | `_scale_` | "The **vector** value…" | it's a single float (`flexi:float`) |
| `XYZToVector` | `_vector list_` | "The list of **x** vector values" | list of vector values |
| `StringSplit` | `_string_` | "The **first** string value to split" | there is only one string input |
| `FlipUV` (descriptor) | `mask` | "A bit mask of primitives **to delete**" | primitives to apply the mode to |
| `SetPointWeight` (descriptor) | `geometry` output | "points at input positions" | output geometry |
| `SortFloatList` (descriptor) | `above index` | "index … of the **'below'** value" | the 'above' value |

### 2.6 Two headings are indented and will not render as headings

- `Extrude/documentation.md` line 50: `  ### Note(s)`
- `UnweldVertices/documentation.md` line 38: `  ### Notes`

CommonMark treats an indented `###` as text, so both sections lose their heading on the live site.

### 2.7 `IntegerValue` — Outputs bullets are missing their `*`

```
#### Outputs

_value_

  * The integer value as defined by the _value_ input.

_input is null_
```

`_value_` and `_input is null_` are plain paragraphs, so the nested description bullets render detached. Add the `* ` prefix.

### 2.8 Broken and non-canonical example links

| Node | URL | Problem |
|---|---|---|
| `Ease` | `…/graph?**asset**=whp:ccc52e9e…` | `asset=` instead of `assetURI=` — link won't open the graph |
| `Ease` | `…&version=**latestt**` | typo in the version param |
| `ExtractPoints` | `…assetURI=whp:8990d4f3…` | missing `&version=latest` |
| `Copy` | `https://**kind-dune-0f6b12f1e.1.azurestaticapps.net**/?assetURI=…` | staging/preview host published in live docs |
| `TessellateCurve` | same staging host ×2 | same |
| `TriangulateCurve` | same staging host ×1 | same |
| `BooleanList`, `Copy2`, `SetColor` | `https://creator.trimble.com/?viewLayout=…` | missing the `/graph` path segment |
| `GeometryInput` | `…assetURI=whp:<uuid>&version=latest` | placeholder inside an HTML comment (intentional TODO, harmless, but worth closing out) |

### 2.9 Broken internal link

`JsonBuilder/documentation.md`: `[**string list**](nodes/StringList/documentation.md)` — **missing the leading `/`**. Every other internal link in the repo uses `/nodes/…`; this relative form will 404 from the JsonBuilder page.

### 2.10 Placeholder text published as content

`ReverseList` and `ReverseStringList` both have an `### Example(s)` section whose only bullet is:

> `* No particular examples at this time. Check back later!`

Either supply an example or drop the section (the playbook says to omit empty sections).

### 2.11 `Circle` deprecation callout is misspelled

`> #### DEPRICATED` and "**Superseeded** by". Already flagged in the playbook as a known typo — worth actually fixing now. `Circle` is also the only node under **Deprecated** in `SUMMARY.md` whose doc otherwise looks non-deprecated (it uses `### Notes` and has no other deprecation signal beyond the misspelled callout).

---

## 3. P2 — Missing and extra inputs/outputs

Full list of the 29 nodes where the doc and descriptor disagree on xputs. "Missing" = in `descriptor.json`, absent from the doc.

### Missing inputs

| Node | Missing input(s) |
|---|---|
| `And` | `value 2`, `value 3`, `value 4` (labelled `value 1` — see §2.2) |
| `Or` | `value 2`, `value 3`, `value 4` (same) |
| `Copy` | `use iterator(s)`, `iterator tag` |
| `Copy2` | `use iterator(s)`, `iterator tag` |
| `Loop` | `combine meshes` |
| `FloatValue` | `step` |
| `Normals` | `scale` |
| `Points` | — (see outputs) |
| `ProjectUV` | `swap U & V`, `flip U`, `flip V`; and `projection axis` is documented as `_axis_` |
| `SetColor` | `edge color`, `edge alpha` |
| `ShiftPrimitiveList` | `shift` |
| `GetAttribute` | `mode`, `type`, `default` (×3) |
| `ExtractUV` | `geometry` |
| `MeshBoolean` | `boolean type` is documented as `_operation type_` |
| `ClosestPointsToPoints` | `calculate distances` is documented as `_calculate distance_` |
| `Cross`, `Dot`, `MultiplyVector`, `SubtractVectors` | descriptor display names are `vector1`/`vector2` (no space); docs write `vector 1`/`vector 2` |
| `Multiply` | descriptor display names `value3`/`value4` (no space); doc writes `value 3`/`value 4` |
| `StringSwitch`, `VectorSwitch` | see §2.3 |

### Missing outputs

| Node | Missing output(s) |
|---|---|
| `Extrude` | **`geometry`** — the node's primary output is undocumented |
| `VectorValue` (Vector) | `x`, `y`, `z` |
| `VectorSwitch` | `vector`, `x`, `y`, `z`, `vector list`, `x list`, `y list`, `z list` |
| `ShiftVectorList` | `vector list`, `x list`, `y list`, `z list` (doc documents a single `_list_` that doesn't exist) |
| `GetAttribute` | `number`, `vector`, `string`, `number list`, `vector list`, `string list` |
| `IntegerValue` | `value`, `input is null` (present but not as bullets — §2.7) |
| `FloatSwitch` | `value`, `value as list` |
| `GetStringListItem` | `string as list` (doc says `_string list_`) |
| `NumPrimitives` | `numPrimitives` (doc says `_number of primitives_`) |
| `Points` | `selection` |

### Enum options that exist but are never mentioned in the doc

| Node | Input | Unmentioned option(s) |
|---|---|---|
| `CurveBoolean` | `fill type` | `even-odd`, `nonzero`, `positive`, `negative` (doc links to a third-party Clipper page instead) |
| `CurveBoolean`, `OffsetCurve`, `TriangulateCurve` | `work plane` | doc writes `X=0` / `Y=0` / `Z=0`; descriptor has `X = 0` etc. (spaces) |
| `OffsetCurve` | `join` | doc writes `simple (none)`; descriptor has `none (simple)` |
| `TriangulateCurve` | `input handling` | doc writes `first curve is outline, **others** are holes`; descriptor has `…other curves are holes` |
| `Normals` | `mode` | doc writes `normals, tangents and binormals (basis)`; descriptor has `tangents, normals, binormals (basis)` |
| `GetAttribute` | `type` | `boolean, integer or float` |

Other enum-case mismatches (doc capitalises, descriptor doesn't): `Align` (`None` vs `none`, ×3), `MeshBoolean` (`Union`/`Subtraction`/… vs lowercase), `CombineData` (`Preserve lists` vs `preserve lists`), `JsonBuilder` (`Array`/`Dictionary` vs `array`/`dictionary`), `FloatValue`/`IntegerValue` (`Soft`/`Hard` vs `soft`/`hard`), `PolyBox` (`csg` vs `CSG`), `PolySphere` (`column & rows` vs `columns & rows`, ×4).

---

## 4. P3 — Content accuracy, wording, and consistency

### Wrong or misleading statements (worth a second opinion — see §6)

- **`Copy`** `_rotate_` example: "a box … copied at a `_rotate_` input of `0,0,45`. The first copy will be rotated by `0,0,45`, the second copy will be rotated another **`45,0,0`**" — should be `0,0,45`.
- **`Copy`** `_scale_` example: "copied at a `_scale_` input of `1,1,1.5`. The first copy will be scaled by **`1.5,1.5,1.5`**" — should be `1,1,1.5` (the stated resulting dimensions `1000,1000,1500` confirm it).
- **`PolyBox`**: "The scale of a box in both the `_scale_` and `_uniform scale_` inputs are **additive**" — these look multiplicative. Please confirm.
- **`Magnitude`** `_square magnitude_`: doc says "Sets whether to **square** the resulting magnitude"; descriptor says "do not take square root after squaring values (faster)". Different operations.
- **`SimplifyCurve`** `_angle threshold_`: doc says "the **maximum** angle from which a curve is simplified"; descriptor says "angle between line segments **above which** to discard the point". Reads inverted.
- **`SetMaterial`** `_bump_`: doc says "between a range of `0` and `1`"; descriptor range is **-10 to 10**.
- **`SetMaterial`** `_incandescence_`: described as "(between a range of `0` and `1`)" but it's a colour input.
- **`GeometryBounds` / `GeometryCentroid`** `_output opposite_`: "Sets whether to **invert** the output geometry bounds/center or not" — vague and probably not what the flag does (likely swaps min/max). Needs a real description.
- **`ColorValue`**: "Any input value above `1` will be **rounded back down** to `1`" — that's clamping, not rounding. Also "The `0` - `1` range **is the same as** the RGB `0` - `255` range" — it maps to it.
- **`MeshBoundary`**: the note refers to the **`_boolean mask_`** output; the output is called `boundary mask`.
- **`TessellateCurve`**: `_segments_` says "when the `_mode_` input is set to **`# of primitives`**" — the option is `# of segments`.
- **`Ephemeral`**: links "the **`Switch`** node" to `/nodes/FloatSwitch/documentation.md` (which is *Number switch*). There is a separate `Switch` node — the link and the label disagree.
- **`Switch`**: refers to "the **`Ephemeral State`** node" but links to `/concepts/GeneralConcepts/ephemeralState.md`, not `/nodes/Ephemeral/documentation.md`.
- **`ExtrudeCurve`**, **`PointsToCurve`**, **`Line`**: `_order_` is described as "the order of the output **line**"; for `ExtrudeCurve` the output is a NURBS **surface**.
- **`GeometryAsset`**: "Other names" lists **STL**, but the supported-format note lists only TrimBIM, IGES, OBJ and DXF. Is STL supported or not?
- **`ExpressionParser`**: the doc's operator list adds **`pi`**, which is absent from the descriptor's list. `Formula`'s list omits it. Which is right?
- **`WeldVertices`** `_mask_`: "defines which **vertices** to weld" — the descriptor's `mask` is a `list:boolean`, which elsewhere in the set is always per-primitive. Please confirm granularity.
- **`EqualVectors`**: summary says "(almost) equal" but the node has **no tolerance input** (unlike `Equal`). Either the wording or the descriptor is wrong.
- **`AngleBetween`**: the note ends mid-thought, has no closing period, and calls a third *vector* a third *angle*.

### Duplicated / redundant prose

- **`BooleanList`** states the same rule twice: "any values manually entered into the `_list_` input will be replaced with the `_default_` input value" and "manually inputted values will be overridden by the `_default_` input value".
- Identical one-line summaries on node pairs where the V1 should differentiate itself: `AddVectors`/`AddVectorsV2`, `Circle`/`CircleV2`, `RandomVector`/`RandomVectorV2`, `ExpressionParser`/`Formula`, `SetListItems`/`SetVectorListItems` (the last is the §2.5 bug).
- **`RandomVectorV2`** "Other names" lists **Float** and **Rand** — copy-pasted from `RandomFloat`; the descriptor's `alternateNames` is empty.
- **`MatchNumberLists`** repeats the descriptor's `help` text verbatim as its only note.

### Typos

`TransformPrimitives` → "Other names … **TransfromPrimitives**" (a searchable alias, so worth fixing) · `Ease` → "The list of possible functions **as as** follows" · `Or` → "whether any values **in a** are true or not" · `Switch` → "A special function of **the this** node" · `Null` → "**The** can be helpful" · `Skin` → "more **noticable**" · `ClosestPointsToPoints` → "the `_mode_` **intput**" · `MeshBoolean` → "Edges and vertices**,**" · `SplitPatch` → "**Nurbs**" (should be NURBS per the root style guide) · `Abs` → "eg." (should be "e.g.") · `CombineMeshes` → "if there **are** more than one primitive in **it's**" · `Mirror` → "The `_mode_` **inputs** first three options" · `SmartSize` → "input primitives **original** size" · `Plane` → "in **the the** same axis".

### Title / label mismatches

| Node | Doc title | Descriptor `name` | `SUMMARY.md` label |
|---|---|---|---|
| `CullList` | Cull number list**s** | cull number list | Cull number list |
| `Ephemeral` | Ephemeral | ephemeral **state** | Ephemeral state |
| `StringSplit` | Split string**s** | split string | Split string |
| `ExtractPoints` | Get **P**oints | get points | Get points |
| `SplitPatch` | Split **S**urface | split surface | Split surface |
| `WeldVertices` | Weld **V**ertices | weld vertices | Weld vertices |
| `FindInStringList` | Find in string list | find in string list | Find **string in** list |
| `GetPrimitive` | Get primitive | get primitive | Get **primtive** |
| `ReversePrimitiveList` | Reverse primitive list | reverse primitive list | Reverse **primtive** list |
| `ShiftPrimitiveList` | Shift primitive list | shift primitive list | Shift **primtive** list |

The three "primtive" typos are in the live sidebar.

### `alternateNames` not carried into the "Other names" bullet

29 nodes. The bigger omissions: `SetMaterial` (8 missing: shading, roughness, reflectance, albedo, opacity, transparency, emission, bump), `TriangulateCurve` (5), `VectorList` (4), `CurveBoolean` (4), `ClosestPointsToPoints` (2), `Collect` (2), `Copy2` (2), `GeometryBounds` (2), `JoinCurves` (2), `Less` (2), `BooleanValue` (2). Full list is reproducible from the script in §7.

Conversely, several docs invent aliases that aren't in the descriptor — `CullList` ("Split list"), `EnumValue` ("Enum"), `GraphAsset` ("Subgraph"), `GetPrimitive` ("Isolate"), `JsonBuilder` ("JSON string"), `Line` ("Curve", "Polyline"), `Modulo` ("Mod"), `Not` ("Invert boolean"), `PolyClean` ("Clean poly"), `StringList` ("Word list"), `TriangulateCurve` ("Path to mesh"), `RandomVectorV2` ("Float", "Rand"). Worth deciding whether the docs or the descriptors are the source of truth for aliases — right now it drifts both ways.

Formatting of that bullet is also inconsistent: 13 nodes omit the "and" before the final item, and 5 use "or" instead of "and" (`BooleanValue`, `GetListItem`, `GetStringListItem`, `GetVectorListItem`, `StringListToString`).

### Playbook style deviations

- `### Inputs` / `### Outputs` at H3 instead of H4: `VectorValue`.
- Legacy `### Notes` instead of `### Note(s)`: 36 files.
- Legacy `### Examples` instead of `### Example(s)`: ~40 files.
- H4 `#### Note(s)` / `#### Example(s)`: `Copy2`.
- Missing the `---` divider entirely: `Ephemeral`, `SimplexNoise`, `Sin`.
- Only one blank line after `---` (playbook wants two): `EnumValue`, `IntegerValue`, `Mirror`, `ReversePrimitiveList`, `ShiftPrimitiveList`, `SmartSize`, `SplitPatch`, and 4 others.
- Irregular bullet indentation that risks mis-nesting: `ReversePrimitiveList`, `ShiftPrimitiveList` (`*  **_geometry_**` with two spaces, 3-space child bullets).
- Stray space inside italics — breaks the emphasis span: `Copy` (`_rotate _input`), `IntegerList` (`_list _input`), `Plane` (`_width _input`).
- Non-bold internal link text: `Power` links `[Expression]` unbolded; the convention elsewhere is `[**Expression**]`.
- 23 files don't end with a newline; 10 have trailing whitespace lines.
- `Round`, `Ceiling`, `Floor` lack the "represented as `round()`/`ceil()`/`floor()` in the **Expression** node" note that every other math node of the same class carries, even though those operators are in the Expression list. Same for `Clamp` (`min`/`max`) and `Max`/`Min`.

### Two concept pages exist but aren't in `SUMMARY.md`

- `concepts/GeneralConcepts/destructive.md` — actively linked from `CombineMeshes` and `MeshBoolean`, so readers can reach it, but it's not in the sidebar.
- `concepts/GeneralConcepts/misc.md` — not linked from anywhere. Dead page?

### `SUMMARY.md` placeholders still open

Ten deprecated/unclassified entries have empty links and inline TODO comments: Create Material (×2 — listed twice, in *Deprecated* and *Missing*), Set Material, Combine Meshes (V1), Extrude (V1), Add Vectors (V2), String Split (V1), Geometry Input (V1), Create Material (V1), Apply Material. Note that *Add Vectors (V2)* is empty even though `AddVectorsV2` **is** documented and already linked under *Vector math* — that entry could just be deleted.

### Playbook itself is slightly out of date

`DOCUMENTATION_PLAYBOOK.md` says it was derived from "all **174** existing `documentation.md` files" (there are now 177) and asserts "**No images are currently used in any node doc**". Five docs use images and all five files exist: `Copy2/usingCopyUsingVectors.png`, `Cross/CrossProduct.png`, `Range/RangeDiagram.gif`, `Skin/interpolate.png`, `SmartSize/SmartSizeDiagram.png`. The playbook should document the `<p align="center"><img …>` pattern those use rather than forbidding images.

---

## 5. Suspected descriptor-side bugs (raise with engineering, not doc fixes)

These look like problems in `@materia/node-descriptors` itself. They surface in the app's node UI, so fixing them there is better than papering over them in the docs.

**Display names that aren't human-readable** (docs are forced to print camelCase):

- `GeometryBounds`: `xMin`, `yMin`, `zMin`, `xMax`, `yMax`, `zMax`
- `GeometryCentroid`: `centerX`, `centerY`, `centerZ`
- `GeometrySize`: `sizeX`, `sizeY`, `sizeZ`
- `NumPrimitives`: `numPrimitives`
- `PointGrid`: `resolutionX`, `resolutionY`, `resolutionZ`
- `Plane`: `orderU`, `orderV`
- `TesselatePatch`: `qualityU`, `qualityV`
- `GetVectorListItem`: `errorMode`
- `SetListItems`, `SetVectorListItems`: `indexList`
- `PointsToCurve`: `keepIncomingGeo`

**Display names missing a space before the number** (inconsistent with siblings, which all use `value 1`):

- `Cross`, `Dot`, `MultiplyVector`, `SubtractVectors`: `vector1`, `vector2`
- `Multiply`: `value3`, `value4` (while `value 1`, `value 2` have the space — inconsistent *within one node*)

**Off-by-one label**: `StringSwitch` keys are `string0`–`string3` but display as `string 1`–`string 4`, while `index` is 0-based. `FloatSwitch` and `VectorSwitch` both label from 0. One of the three is wrong.

**Typos in descriptor text:**

- `SetPointWeight`: `alternateNames` contains **`"weigth"`**
- `GetPrimitive`: `index` description reads "…incoming list of primitives **9list** of indices also allowed)"
- `Atan2`: help reads "of two values (x **an** y)"
- `SimplifyCurve`: help reads "Simplifies **inputs** curves using **a** angle threshold"
- `CombineStringLists`: help reads "Joins string **list**" (singular)

**Copy-paste errors in descriptor text:** `FlipUV` `mask` ("to delete"), `SetPointWeight` geometry output ("points at input positions"), `SortFloatList` `above index` ("the 'below' value"), `EqualVectors` help ("Checks whether **values** are (almost) equal" — should say vectors).

**Stale help:** `UnrollCurve` help says "Unrolls each curve along **x axis**" but the node has `origin` and `direction` inputs.

**Duplicate `defaultNodeName`** — two different nodes get the same name when created:

| Name | Nodes |
|---|---|
| `number` | `FloatValue`, `IntegerValue` |
| `number list` | `FloatList`, `IntegerList` |
| `add vectors` | `AddVectors`, `AddVectorsV2` |
| `circle` | `Circle`, `CircleV2` |
| `random vector` | `RandomVector`, `RandomVectorV2` |
| `tetrahedron` | `Tetrahedron`, `TetrahedronV2` |

The V1/V2 pairs are expected; **`FloatValue`/`IntegerValue` and `FloatList`/`IntegerList` are not** — two live, non-deprecated nodes both default to "number" / "number list".

**Other descriptor oddities:**

- `Null`: `defaultNodeName` is an empty string.
- `TessellateCurve`: folder is `TessellateCurve` but `type` is `TesselateCurve` (one `l`). Whichever is authoritative, the other is wrong — and this is the only folder/type mismatch in the set.
- `Collect`: `alternateNames` includes **`"test"`** — looks like leftover debris.
- `Less`: `alternateNames` includes `"less"`, i.e. its own name.
- `Loop`, `Copy`: `alternateNames` includes `"loop"` (Loop's own name).
- 37 descriptors have no `help` field at all, including high-traffic nodes: `Align`, `AddAttribute`, `CombineMeshes`, `Copy`, `CurveBoolean`, `Extrude`, `ExtrudeCurve`, `GeometryAsset`, `GeometryBounds`, `GeometryCentroid`, `GeometrySize`, `GetAttribute`, `GroupPrimitives`, `Iterator`, `Line`, `Locator`, `Loop`, `Mirror`, `OffsetCurve`, `Plane`, `PointGrid`, `PolyBox`, `PolyCylinder`, `PolySphere`, `SetColor`, `SetMaterial`, `Skin`, `SmartSize`, `Switch`, `TetrahedronV2`, `TriangulateCurve`, `UnGroupPrimitives`, `UnweldVertices`, `WeldVertices`, `CircleV2`, `Null` (has one), `GeometryInput` (has one). Node-picker tooltips are presumably empty for these.

---

## 6. Questions for you

1. **Should I pull `@materia/node-descriptors@32.3.16` and re-run this as a three-way diff?** It needs either artifactory npm auth in the session or you running `npm install` / `npm pack @materia/node-descriptors` in `materia-creator` once. Without it I can't tell a stale descriptor from a stale doc.
2. **Aliases: docs or descriptors as source of truth?** Roughly a dozen docs list aliases that don't exist in `alternateNames`, and 29 descriptors have aliases the docs don't mention. If the docs are meant to mirror the descriptor exactly (as the playbook says), the invented ones should go; if the docs are where new aliases get proposed, the descriptors need updating from them.
3. **`Copy` rotate/scale examples** — can you confirm the corrected values in §4 before I edit? The arithmetic points one way but I'd rather you sanity-check the node's actual behaviour.
4. **`PolyBox` "additive" scale** — multiplicative, I assume?
5. **STL support in `GeometryAsset`** — supported (and the format list needs it added) or not (and the alias should go)?
6. **`pi` in the Expression operator list** — supported? The `ExpressionParser` doc claims it, the descriptor doesn't list it, and `Formula` omits it.
7. **`misc.md`** — is that concept page still wanted? It's linked from nowhere and absent from `SUMMARY.md`.
8. **The V1 "Deprecated" placeholders in `SUMMARY.md`** — do you want me to write the missing V1 docs (Combine Meshes, Extrude, String Split, Geometry Input, Create/Apply/Set Material), or delete the entries? *Add Vectors (V2)* in particular is a duplicate of a page that already exists.
9. **Want me to start fixing?** I'd suggest three PRs off `dev`: (a) P1 only — the ten items in §2, small and reviewable; (b) the 29 nodes with xput gaps; (c) style/consistency sweep. Say the word and I'll start with (a).

---

## 7. Reproducing this

The scripts live in the session workspace (`~/review/` on the linked machine, not in the repo):

- `analyze.py` — xput coverage, titles, enum options, alternate names, links, `SUMMARY.md` wiring → `findings.json`
- `analyze2.py` — headings, descriptor display names, deprecation, example anchors, duplicate prose → `findings2.json`
- `analyze3.py` — relative links, non-canonical URLs, conjunctions, whitespace, duplicate `defaultNodeName`, orphan concept pages
- `corpus.py` — flattens all 177 descriptor+doc pairs into one reviewable file

Tell me if you want them committed into the repo as a CI check — a trimmed version of `analyze.py` would make a good pre-commit hook for the "every xput must be documented" rule the playbook already asks for by hand.
