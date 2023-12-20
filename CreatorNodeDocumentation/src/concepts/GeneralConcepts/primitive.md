# Primitive

---

Primitives are a [graph's](/concepts/GeneralConcepts/graph.md)'s computed entities. They are created and transformed by [nodes](/concepts/GeneralConcepts/node.md), and flow through the nodes and [connections](/concepts/GeneralConcepts/connection.md) of a graph.

Examples of primitives:

* [`PolyMesh`](/concepts/GeneralConcepts/polyMesh.md): a 3D polygonal mesh primitive.
* [`NURBS curve`](/concepts/GeneralConcepts/nurbsCurve.md) and [`NURBS surface`](/concepts/GeneralConcepts/nurbsSurface.md): a <a href="https://en.wikipedia.org/wiki/Non-uniform_rational_B-spline" target="_blank">NURBS</a> curve and NURBS surface primitive.


Consider this graph:

<p align="center">
  <img width="600" src="images/CollectSphereAndCircle.png"/>
</p>

The [**circle**](/nodes/CircleV2/documentation.md) node creates a [`NURBS curve`](/concepts/GeneralConcepts/nurbsCurve.md) primitive, and the [**sphere**](/nodes/PolySphere/documentation.md) node creates a [`PolyMesh`](/concepts/GeneralConcepts/polyMesh.md) primitive.


<p align="center">
  <img width="600" src="images/CircleAndSphere.png"/>
</p>

Both primitives get passed downstream to the [**collect**](/nodes/Collect/documentation.md) node. In its turn, the [**collect**](/nodes/Collect/documentation.md) node passes the two collected primitives on downstream to any node connected to its output.

<p align="center">
  <img width="600" src="images/PrimitiveFlow.png"/>
</p>

In this case, the primitives pass through the [**collect**](/nodes/Collect/documentation.md) node unchanged, but other node types have the ability to transform and modify incoming primitives. Example: an [**extrude mesh**](/nodes/Extrude/documentation.md) node will extrude the polygons of any incoming [`PolyMesh`](/concepts/GeneralConcepts/polyMesh.md) primitive, but not [`NURBS curve`](/concepts/GeneralConcepts/nurbsCurve.md) primitives.