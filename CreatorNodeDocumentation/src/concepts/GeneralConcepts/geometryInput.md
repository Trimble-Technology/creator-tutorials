# Geometry input

---

A geometry input is how geometry that was *not* authored inside a [graph](/concepts/GeneralConcepts/graph.md) gets into it.

Most graphs build every [primitive](/concepts/GeneralConcepts/primitive.md) they output, either from creation nodes or from an uploaded [asset](/concepts/GeneralConcepts/assets.md). A geometry input works the other way around: the geometry is supplied to the graph at [compute](/concepts/GeneralConcepts/compute.md) time by whatever is hosting it, and the graph reacts to whatever it is given. The graph doesn't own that geometry — it responds to it.

This is the mechanism behind [AutoFit](/concepts/GeneralConcepts/autoFit.md) for [Live Components](/concepts/GeneralConcepts/liveComponent.md).


### In Graph

Geometry enters through the [**geometry input**](/nodes/GeometryInput/documentation.md) node.

The node's *json geometry* input takes a JSON encoded string and parses it into [primitives](/concepts/GeneralConcepts/primitive.md) on its **_geometry_** output, along with the flattened point data (*points*, *points.x*, *points.y*, and *points.z*) for driving the rest of the graph.

Two primitive types can be parsed — a [polyline](/concepts/GeneralConcepts/nurbsCurve.md) or a [PolyMesh](/concepts/GeneralConcepts/polyMesh.md) — either singularly or as an array of them. The expected JSON format follows the definitions in the <a href="https://github.com/Trimble-Technology/eidos-json-schema" target="_blank">eidos-json-schema</a> repository.

Because the input is a plain string, a geometry input can be authored and tested entirely inside Trimble Creator by pasting JSON straight into the *json geometry* input — no host application required.

The optional *geometry schema* input takes a JSON schema that the incoming geometry is validated against, which is how a graph can reject geometry it isn't built to handle. Leaving it empty parses the geometry without validating it.


### In Situ

When a [Live Component](/concepts/GeneralConcepts/liveComponent.md) is applied to a face in SketchUp, that face is converted to JSON and enters the graph through the [**geometry input**](/nodes/GeometryInput/documentation.md) node. The graph recomputes and the Live Component regenerates against that geometry.

<!-- TODO: confirm the exact SketchUp-side wording for applying an LC to a face, and add a GIF here (see images/ folder) once one is available. -->


### Notes

* A geometry input has no geometry of its own. Its default *json geometry* value is an empty polyline (`{"id":"emptyPolyLine","points":[]}`), so a graph should still resolve sensibly when nothing has been supplied to it — see the [AutoFit](/concepts/GeneralConcepts/autoFit.md) concept page for ways to guard against this.

* Only the geometry described by the schema comes through. A geometry input carries point and face data, not [materials](/concepts/GeneralConcepts/material.md) or [attributes](/concepts/GeneralConcepts/attribute.md) — anything like that has to be added inside the graph.

* A geometry input is distinct from a [**geometry asset**](/nodes/GeometryAsset/documentation.md) node. An asset is uploaded ahead of time and referenced by the graph; a geometry input is handed to the graph each time it computes.
