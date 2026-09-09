# Geometry input

**_Parses JSON encoded geometry into geometry primitives._**

---


#### Inputs

* _json geometry_

  * The JSON encoded string that defines the geometry to parse. This can be a single polyline or PolyMesh, or an array of them.
    * Defaults to an empty polyline (`{"id":"emptyPolyLine","points":[]}`), which parses to no geometry at all.

* _geometry schema_

  * An optional JSON schema to validate the incoming _json geometry_ against. Leave this empty to parse the geometry without validating it.


#### Outputs

* **_geometry_**

  * Output geometry primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Note(s)

* This node is how geometry authored outside of the graph gets into it — most graphs build every primitive they output, but a graph using this node instead reacts to whatever geometry it is given at [**compute**](/concepts/GeneralConcepts/compute.md) time.

* When a [**Live Component**](/concepts/GeneralConcepts/liveComponent.md) is applied to a face in SketchUp, that face is converted to JSON and enters the graph through this node. This is what makes [**AutoFit**](/concepts/GeneralConcepts/autoFit.md) possible.

* The expected JSON format follows the polyline and PolyMesh definitions in the <a href="https://github.com/Trimble-Technology/eidos-json-schema" target="_blank">eidos-json-schema</a> repository. Only those two [**primitive**](/concepts/GeneralConcepts/primitive.md) types are supported — a [**NURBS curve**](/concepts/GeneralConcepts/nurbsCurve.md) or [**NURBS surface**](/concepts/GeneralConcepts/nurbsSurface.md) cannot be parsed by this node.

* Only point and face data comes through. [**Materials**](/concepts/GeneralConcepts/material.md) and [**attributes**](/concepts/GeneralConcepts/attribute.md) are not carried in, so anything like that has to be applied inside the graph.

* Because _json geometry_ is a plain string, geometry can be tested by pasting JSON directly into the input, without a host application supplying it.

* Unlike the [**geometry asset**](/nodes/GeometryAsset/documentation.md) node, which references geometry uploaded to the graph ahead of time as an [**asset**](/concepts/GeneralConcepts/assets.md), this node receives its geometry each time the graph [**computes**](/concepts/GeneralConcepts/compute.md).

* A graph using this node should resolve sensibly when no geometry has been supplied to it — the default empty polyline is what a graph sees before anything has been connected or applied.

* Other names for this node include: GeometryInput.


<!-- TODO: add an Example(s) section once a suitable public example graph exists:
### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:<uuid>&version=latest" target="_blank">Example title</a>
-->
