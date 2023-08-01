# Mesh boundary

**_Creates polyline curves around all mesh boundaries._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).


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

* _boundary mask_

  * The list of boolean values identifying if a vertex was used to create a curve or not.

* _boundary indices_

  * The list of indices of the vertexes that define the resulting boundary.


### Note(s)

* An example of an  instance where a mesh boundary will not be made (and therefore will turn a `false` result in the _boolean mask_ output) might be where mesh edges/boundaries are welded together (and thus not a boundary) or, a primitive type other than a PolyMesh is input into this node.

* Other names for this node include: MeshBoundary, Edges, Contour, and Border.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:fb65c141-bf5f-4646-9acf-630ca39ff972&version=latest" target="_blank">Polyline box</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:728dd414-114f-4668-8f5c-9fb8154d0b79&version=latest" target="_blank">Loft along curve w/ cap</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:1aaa9e16-e112-463e-bf9a-2c990de46a4e&version=latest" target="_blank">Isolate face holes and boundary</a>
