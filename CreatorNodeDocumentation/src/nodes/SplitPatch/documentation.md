# Split Surface

**_Splits NURBS surfaces along a U or V value._**

---

#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _direction_

  * Sets the direction within which to split the surface. This can be `U` or `V`.

* _location_

  * The value at which to split the surface. Accepts values from `0` - `1`.


* _discard_

  * Sets the calculated primitive to delete. This can be `none`, `first`, or `second`.


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

* Other names for this node include: SplitPatch, Split patch, Cut, Nurbs, Carve.

### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:a88ccc3b-46f5-4ce4-ada4-8af43efebb7b&version=latest" target="_blank">Split surface</a>
