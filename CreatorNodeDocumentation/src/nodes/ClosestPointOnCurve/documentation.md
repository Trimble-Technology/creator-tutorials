# Closest point on curve

**_Finds the closest point on an input curve to input points._**

---


#### Inputs

* **_geometry_**

  * The input curves to find closest point on.

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _positions_

  * The list of vector values of the points’ positions.

* _accuracy_

  * The value that determines how accurate the point is found on the input curve.


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

* _distances_

  * The list of distances between the input positions and the found points on the input curve.

* _u coordinates_

  * The list of u coordinates of the found points on the input curve.


### Note(s)

* Other names for this node include: ClosestPointOnCurve, Nearest, and Distance.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:8e562cff-deea-48ef-82eb-dbc810d1920b&version=latest" target="_blank">Closest point on curve</a>
