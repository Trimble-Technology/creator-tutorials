## Triangulate 2d path

**_Converts 2D curves into a triangulated mesh in a chosen workplane._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


#### Inputs

* _work plane_

  * The work plane in which the triangulation will be performed in. These are `X=0`, `Y=0`, and `Z=0`.

* _pre-flatten_

  * Flattens the input curves into the work plane defined by the _work plane_ input before triangulation.

* _library_

  * Sets the triangulation library to triangulate input curves. These are `Poly2Tri` (quicker) and `Triangle` (slower, but offers triangle refinement and smoothing).

* _input handling_

  * Sets how the input curves are handled within the triangulation. These are `first curve is outline, others are holes` (the first input curve is the outline and following input curves are holes within the resulting triangulation) and `all curves are outlines` (all input curves are outlines and no holes are made).

* _make convex hull_

  * Sets whether the resulting triangulation is a convex hull of the input curves or not.

* _algorithm_

  * Sets the algorithm to use for triangulation while the _library_ input is set to `Triangle`. These are `sweepline`, `Dwyer`, and `incremental`.

* _refine_

  * Sets whether or not to manually refine the triangles in the resulting triangulation when the _library_ input is set to `Triangle`.

* _max area_

  * The maximum area of triangles in the resulting triangulation when the _library_ input is set to `Triangle` and the _refine_ input is set to `true`.

* _min angle_

  * The minimum angle of triangles in the resulting triangulation when the _library_ input is set to `Triangle` and the _refine_ input is set to `true`.

* _max angle_

  * The maximum angle of triangles in the resulting triangulation when the _library_ input is set to `Triangle` and the _refine_ input is set to `true`.

* _smoothing_

  * The amount of smoothing of triangle layout after triangulation defined between `0` and `100`.

* _inner points_

  * A list of extra internal points that will force the creation of vertices at these points.


#### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


#### Note(s)



* The `first curve is outline, others are holes` setting of the _input handling_ input results in a single primitive whereas the `all curves are outlines` setting results in a primitive for each input curve.
* If the input curve is irregular and the resulting triangulate mesh results in “zero area triangles”, it is recommended to use the **clean mesh** node to fix the mesh.
* Other names for this node include: Triangulate curve, Tessellate, Mesh, and Path to mesh.


#### Example(s):



* <a href="https://kind-dune-0f6b12f1e.1.azurestaticapps.net/?assetURI=whp:c9ec5808-aa2a-452c-9938-96b9b590aade&version=latest" target="_blank">Triangulate an outline</a>
