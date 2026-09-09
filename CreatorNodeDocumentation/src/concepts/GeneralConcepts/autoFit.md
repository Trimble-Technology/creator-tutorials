# AutoFit

---

AutoFit describes a [Live Component](/concepts/GeneralConcepts/liveComponent.md) that reads geometry from the model around it and rebuilds itself to fit that geometry.

A [size frame](/concepts/GeneralConcepts/sizeFrame.md) lets a user drive a graph's [parameters](/concepts/GeneralConcepts/parameter.md) by stretching grips with the Scale Tool. AutoFit lets a user drive a graph by pointing it at geometry that already exists in their model: apply the Live Component to a face, and the component regenerates to suit that face.

<!-- TODO: confirm this framing against the agreed external terminology for AutoFit / control geometry before this goes to main. -->


### In Situ

When a Live Component authored for AutoFit is applied to a face in SketchUp, that face is converted to JSON and passed into the [graph](/concepts/GeneralConcepts/graph.md) through its [**geometry input**](/nodes/GeometryInput/documentation.md) node. The graph [computes](/concepts/GeneralConcepts/compute.md) against that geometry, and the geometry the Live Component generates changes accordingly.

Because the fit is recomputed rather than baked in, changing the face the Live Component was applied to regenerates the component against the new shape.

<!-- TODO: add a GIF of an LC AutoFitting to a face here (see images/ folder), and confirm the exact SketchUp-side interaction wording. -->


### In Graph

An AutoFit graph is built around a [**geometry input**](/nodes/GeometryInput/documentation.md) node instead of fixed dimensions. See the [geometry input](/concepts/GeneralConcepts/geometryInput.md) concept page for how that node works.

The usual pattern is to measure the incoming geometry, then build against those measurements rather than against [parameter](/concepts/GeneralConcepts/parameter.md) values:

* Measure it with nodes like [**geometry bounds**](/nodes/GeometryBounds/documentation.md), [**geometry size**](/nodes/GeometrySize/documentation.md), and [**geometry center**](/nodes/GeometryCentroid/documentation.md), or work directly from the *points* outputs of the [**geometry input**](/nodes/GeometryInput/documentation.md) node.

* Place and scale against it with nodes like [**align**](/nodes/Align/documentation.md), [**transform**](/nodes/TransformPrimitives/documentation.md), and [**smart size**](/nodes/SmartSize/documentation.md) — [**smart size**](/nodes/SmartSize/documentation.md) is particularly useful here, as it lets a component stretch to an arbitrary incoming size while preserving detail inside its lock zones.

* Distribute repeated detail across it with nodes like [**copy**](/nodes/Copy/documentation.md), [**copy using vectors**](/nodes/Copy2/documentation.md), or [**iterator**](/nodes/Iterator/documentation.md), using the measured size to work out how many copies are needed.


### Notes

* It is up to the author to make sure the graph resolves sensibly for geometry it wasn't expecting. Things worth handling explicitly:

    * Nothing supplied at all — the [**geometry input**](/nodes/GeometryInput/documentation.md) node's default is an empty polyline, so a graph should still produce something reasonable (or nothing at all) before it has been given a face.

    * Geometry outside the range the component was designed for, e.g. a face far smaller or larger than any sensible instance of the component.

    * Geometry of the wrong shape or type, e.g. a non-planar or unexpectedly complex face. The [**geometry input**](/nodes/GeometryInput/documentation.md) node's *geometry schema* input can be used to validate incoming geometry, and the [**error check**](/nodes/Error/documentation.md) node can be used to fail loudly rather than silently generating something wrong.

* Guard branches with a [**switch**](/nodes/Switch/documentation.md) node (or a [**number switch**](/nodes/FloatSwitch/documentation.md) / [**string switch**](/nodes/StringSwitch/documentation.md) for values) so the graph can fall back to a default result when the incoming geometry isn't usable.

* AutoFit and a [size frame](/concepts/GeneralConcepts/sizeFrame.md) can both be present in the same Live Component, but be deliberate about it — if a size frame drives the same dimensions the incoming geometry does, the two will fight, and it won't be obvious to a user which one is in control.

* Keep an eye on how much the graph rebuilds. Every change to the geometry a Live Component is fitted to triggers a full [compute](/concepts/GeneralConcepts/compute.md), so the cost of an AutoFit graph is paid on every edit, not just on placement.


### Examples

<!-- TODO: add example graph links in the standard format once suitable public example graphs are picked:
* <a href="https://creator.trimble.com/graph?assetURI=whp:<uuid>&version=latest" target="_blank">Example title</a>
-->
