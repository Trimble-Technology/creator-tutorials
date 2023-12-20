# Collect

**_Collects all primitives from all geometry inputs into a single geometry output._**

---


#### Inputs

* **_geometry_**

  * Accepts multiple geometry connections.


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

* This node simply gathers incoming primitives into a list, arranging them in the order of their associated geometry input connections.
* Other names for this node include: Merge and Collate.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:bd275731-a867-47d1-8bfa-16151c9b6c60&version=latest" target="_blank">Collect</a>