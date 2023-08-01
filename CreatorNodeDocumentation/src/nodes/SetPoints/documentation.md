# Set points

**_Sets the position of points using xyz values._**

---


### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _x_

  * The x value of the vector position to set input points to.

* _y_

  * The y value of the vector position to set input points to.

* _z_

  * The z value of the vector position to set input points to.

* _mask_

  * The list of boolean values that defines which input points to set to the vector as defined by the _x_, _y_, and _z_ inputs. If empty, all input points will be set to the defined vector.


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


### Notes

* Other names for this node include: SetPoints, and Set positions.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:2f334829-4e60-48ae-8e0c-3412fabbed23&version=latest" target="_blank">Setting a point within a polyline</a>
* <a href="https://creator.trimble.com/graph?assetURI=whp:2cdc8040-63ba-4cb1-875b-30e3e195e1a2&version=latest" target="_blank">Apply a trigonometric function to a line</a>
