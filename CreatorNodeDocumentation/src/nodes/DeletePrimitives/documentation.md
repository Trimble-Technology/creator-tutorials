# Delete primitives

**_Deletes primitives using a mask or index list._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _mask_

  * The list of boolean values that defines which primitives to delete.

* _index list_

  * The list of indices that defines which primitives to delete.

* _invert_

  * Sets whether to invert the selection of deleted primitives or not.

* _keep points_

  * Sets whether to keep the points of deleted primitives or not.


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

* Other names for this node include: DeletePrimitives, Erase, and Nuke.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:65e34b44-9167-4a3b-af5e-8414812113c7&version=latest" target="_blank">Delete primitives with a boolean pattern</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:1aaa9e16-e112-463e-bf9a-2c990de46a4e&version=latest" target="_blank">Isolate face holes & boundary</a>