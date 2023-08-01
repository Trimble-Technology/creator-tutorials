# Clean mesh

**_Attempts to clean up "dirty" polygonal geometry._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _nuke small triangles_

  * Sets whether to delete small triangles or not. The area of the nuked triangles is set by the _area threshold_ input.

* _area threshold_

  * The minimum area that determines if a triangle is nuked when _nuke small triangles_ is set to `true`.

* _nuke orphan points_

  * Sets whether to delete points not associated with any triangles or not.


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


### Note(s)

* Other names for this node include: PolyClean, Delete zero area, and Clean poly.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:46064975-47b6-4e33-b065-ad654750379e&version=latest" target="_blank">Clean mesh</a>
