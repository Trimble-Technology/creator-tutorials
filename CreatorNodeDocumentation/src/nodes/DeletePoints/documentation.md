# Delete points

**_Deletes points using a mask or index list._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mask_

  * The list of boolean values that defines which points to delete from input primitives.

* _index list_

  * The list of indices that defines which points to delete from input primitives.

* _invert_

  * Sets whether to invert the selection of deleted points or not.


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

* This node will delete points from almost any input primitives with some exceptions:

  * [NURBS surfaces](/concepts/GeneralConcepts/nurbsSurface.md).

  * Polylines/[NURBS curves](/concepts/GeneralConcepts/nurbsCurve.md) where the resulting curve will be left with only a single point.

* Other names for this node include: DeletePoints, Erase, and Nuke.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:9e74813e-267b-49b9-bc9d-98c84cf5aca8&version=latest" target="_blank">Delete points with a boolean pattern</a>