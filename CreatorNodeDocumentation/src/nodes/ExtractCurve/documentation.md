# Curve from surface

**_Extracts a curve from a NURBS surface using U or V coordinate values._**

---


### Inputs

* **_geometry_**

 * Accepts a single geometry connection (unless the SHIFT key is held).

* _location_

  * The value that defines the coordinate of where to extract the curve from the input surface.

* _along U_

  * Sets whether to extract the curve from the surface’s u coordinate or not. If false, the node will use the v coordinate.


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

* Other names for this node include: Isoparm, Extract curve, and NURBS patch.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:83299957-754d-4f34-b5b3-a729802f551e&version=latest" target="_blank">Extract curve from surface</a>