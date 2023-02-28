# Rectangle

**_Creates a rectangular plane._**

> This node has data inputs and outputs.
>
> This node has geometry inputs and outputs.


### Inputs

* _type_

  * Sets the type of rectangle to output. This can be `NURBS surface`, `points`, `mesh`, or `polyline`.

* _orientation_

  * Sets the plane in which the output rectangle is orientated. This can be `XZ`, `YZ`, or `XY`.

* _center_

  * The vector value that defines the center of the output rectangle.

* _length_

  * The value that defines the length dimension of the output rectangle.

* _width_

  * The value that defines the width dimension of the output rectangle.

* _orderU_

  * The value that defines the order of the U axis of the output rectangle (in the same axis as the _width _input) when the _type_ input is set to `NURBS surface`. See <a href="/concepts/GeneralConcepts/nurbsSurface.md" target="_blank">NURBS surface</a> for more information.

* _orderV_

  * The value that defines the order of the V axis of the output rectangle (in the the same axis as the _length _input) when the _type_ input is set to `NURBS surface`. See <a href="/concepts/GeneralConcepts/nurbsSurface.md" target="_blank">NURBS surface</a> for more information.

* _point columns_

  * The value that defines the number of point columns along the same axis as the _width_ input.

* _point rows_

  * The value that defines the number of point rows along the same axis as the _length _input.


### Outputs

* _points_

  * The list of points of the output primitives.

* _points.x_

  * The list of x values of the points of the output primitives.

* _points.y_

  * The list of y values of the points of the output primitives.

* _points.z_

  * The list of z values of the points of the output primitives.


### Notes



* Other names for this node include: Plane, Square, Grid, and Patch.


### Examples



* <a href="https://creator.trimble.com/graph?assetURI=whp:ef3ef267-3457-402c-a7b6-5729ad36dac3&version=latest" target="_blank">Rectangle</a>
