# Boolean 3D geometry

**_Performs boolean operations on 3D geometry._**

---


#### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.

* _operation type_

  * Sets the type of boolean operation to perform on input geometry. This can be: `Union`, `Subtraction`, Reverse subtraction`, `Intersection`, or `XOR`.

* _weld_

  * Sets whether to pre-weld input geometry or not.


#### Outputs

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


### Note(s)

* This node specifically operates on [PolyMesh](/concepts/GeneralConcepts/polyMesh.md) type primitives. Therefore there are a couple things to keep in mind to get consistent results when using this node:

  * Avoid coplanar faces

    * Specifically this means geometry that is being operated on has faces that are within the same plane as each other (one example may be when unioning two boxes that have been aligned directly next to each other, where one side of each box touches a side of another). Often stretching an input geometry (with either the [**transform**](/nodes/TransformPrimitives/documentation.md) or [**smart size**](/nodes/SmartSize/documentation.md) nodes) so that there is a clear overlap, can help with more consistent behavior.

  * Edges and vertices,

    * A mesh 3D boolean operation utilizes vertices and edges of input meshes to perform operations. Therefore, it is often useful to pay attention to where particular geometries are positioned. Say for example we have a box that is subtracting from another box where the position of the subtracting box is positioned so that it lies directly in the middle of a triangle of the first box's mesh. In this instance, there are no intersecting edges or vertices of either mesh, thus making it difficult to calculate consistently.

* Other names for this node include: 3D boolean, Mesh boolean, and CSG.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:b289a76d-c470-4d84-bf40-85f14084622e&version=latest" target="_blank">Boolean 3D geometry</a>
