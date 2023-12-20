# Weld Vertices

**_Welds overlapping polygon triangle edges based on an angle threshold._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _radius_

  * The radius that determines if adjacent vertices will be welded together.

* _angle threshold_

  * The minimum angle that determines if adjacent vertices will be welded together.

* _average position_

  * Sets whether to average the position of welded vertices or not.

* _nuke ghost triangles_

  * Sets whether to delete triangles with zero area (that can often occur by the weld). This is done after the weld.

* _nuke orphan points_

  * Sets whether to delete points not associated with any triangles. This is done after the weld.

* _mask_

  * The list of boolean values that defines which vertices to weld together. If empty, all vertices will be welded together.


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


### Notes

* Other names for this node include: WeldVertices, Smooth normals, Merge points, and Weld polygons.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:3ea02aa1-c685-4932-960e-0580ebcf86ed&version=latest" target="_blank">Weld angles</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:f419f1c8-f85f-4f92-b5f4-f0e8f6379a43&version=latest" target="_blank">Unwelded v. welded number of points</a>
