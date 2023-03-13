# Extrude curve

**_Extrudes curves in a vector direction._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _extrusion_

  * The vector value that defines the extent that the output NURBS surface primitive will be extruded.

* _order_

  * The value that defines the order of the output line. See [NURBS surface](/concepts/GeneralConcepts/nurbsSurface.md) for more information.

* _number of spans_

  * The number of spans that the output NURBS surface will be divided into.


### Outputs

* **_geometry_**

  * Output primitives.

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes



* The geometry output of this node is a NURBS surface primitive type. In order to convert it to a PolyMesh primitive type use the **triangulate surface** node.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:fb5b6019-be5a-4bc8-b2a4-624287e4a444&version=latest" target="_blank">Extrude curve</a>
