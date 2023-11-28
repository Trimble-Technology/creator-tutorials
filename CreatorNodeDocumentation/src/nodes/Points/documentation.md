
# Points

**_Creates points at input positions._**

---


### Inputs

* _positions_

  * The list of vector values that define the positions where points are created.

* _initialize_

  * Sets the _positions_ input vector values to the vector values as defined by the _init list_ input.

* _init list_

  * The list of vector values that will be output when initialized.

* _output as mesh vertices_

  * Sets whether the output primitives are as [Points primitives](/concepts/GeneralConcepts/points.md) or [PolyMesh](/concepts/GeneralConcepts/polyMesh.md) vertices.


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

* If the _positions_ input has a list of vectors connected to it, then the connected input will override the values in _init list_ when initialized.

* Other names for this node include: Create points.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:17b7d74c-68b8-4c82-bc2c-6398f96556e6&version=latest" target="_blank">Points</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:fe2a797b-58c5-4a2e-941d-bcae38ae6515&version=latest" target="_blank">Points to curve</a>
