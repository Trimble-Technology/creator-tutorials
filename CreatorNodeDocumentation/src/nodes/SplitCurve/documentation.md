# Split curve

**_Splits curves into parts, or extracts the splitting point._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _u_

  * The value that defines the u coordinate of where to split the input curve.

* _split points only_

  * Sets whether to output only the splitting point or not.


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

* Very similar functionality to the [**Insert knot**](/nodes/InsertKnot/documentation.md) node. Both nodes apply a point to a line, where this node will divide a curve into two separate primitives (or a single point), whereas the [**Insert knot**](/nodes/InsertKnot/documentation.md) node will place a point on that curve.

* Other names for this node include: SplitCurve, Cut, and Carve.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:2de95a82-2dc8-4edd-888c-e3f28c56b1ee&version=latest" target="_blank">Split curve</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:27966e4f-e1dd-448a-b70f-08a20bedfd71&version=latest" target="_blank">Split curve by length</a>
