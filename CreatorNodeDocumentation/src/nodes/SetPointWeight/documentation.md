# Set point weight

**_Sets point weights._**

---


#### Inputs

* **_geometry_**

  * Accepts a single geometry connection (unless the SHIFT key is held).

* _weights_

  * The list of float values that defines the weight of points in a NURBS primitive (curves and surfaces). 

* _default weight_

  * The weight value that defines the weight of all points when no data is connected to the _weights _input.


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

* Sets the weight value of input geometry points based on input data values for use in NURBS curves and surfaces.

* The weight value’s effect exhibits an exponential decay pattern as the ratio between points increases, e.g the difference between a weight ratio of 0 and 2 is less than twice the difference between a weight ratio of 0 and 1.

* If _default weight_ is in use all points will have the same weight so the exact value is irrelevant unless set to ‘0’ in which case no geometry will be generated.

* Other names for this node include: Edit point weight, Weight.


### Example(s)

* <a href="https://creator.trimble.com/graph?assetURI=whp:fda9e49d-ec22-4f59-bf1b-388973b49b08&version=latest" target="_blank">Adjusting the weight of a control point in a NURBS curve</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:be6d8d9c-71b0-49c9-a46f-a1adfa531cb7&version=latest" target="_blank">Adjusting multiple control points in a NURBS curve</a>

* <a href="https://creator.trimble.com/graph?assetURI=whp:91003498-1edb-4de9-afa0-c31086a66e51&version=latest" target="_blank">Adjusting the weight of a control point in a NURBS surface</a>