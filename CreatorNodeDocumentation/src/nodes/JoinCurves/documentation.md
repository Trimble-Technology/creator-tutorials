# Join curves

**_Joins curve ends using a distance threshold._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _tolerance_

  * The value that defines the maximum distance by which two curves will be joined.

* _delete last point_

  * Sets whether to delete the last point of every joined curve or not.


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

* The _tolerance_ unit will be the set unit of the graph.

* Other names for this node include: JoinCurves, Merge curves, Connect curves, and Combine curves.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:00d521e3-ed64-42c9-aaec-f22a9c91b8a6&version=latest" target="_blank">Simple wave</a>

* <a href="https://creator.trimble.com/graph?layout=right&assetURI=whp:cb18b98f-ec31-4a50-ac7a-8dc740da92f3&version=latest" target="_blank">Select polygon edges</a>
