# Insert knot

**_Inserts a control point on a curve._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _u_

  * The value that defines the u coordinate of where to insert a point in the curve.


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

* Very similar functionality to the [**Split curve**](/nodes/SplitCurve/documentation.md) node. Both nodes apply a point to a line, while this node will place a control point on that curve, where as the [**Split curve**](/nodes/SplitCurve/documentation.md) node will divide that curve into two separate primitives (or a single individual point).

* Other names for this node include: InsertKnot, Add point.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:4d0ee07f-1d23-41a2-bd20-4e7a85b9652d&version=latest" target="_blank">Insert knot by distance</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:0d867031-2f75-45ce-b9b7-53152d8f29d4&version=latest" target="_blank">Insert knot to create polyline</a>
